<template>
  <div>
    <section class="breadcrumbs">
      <Breadcrumbs />
      <Nuxt />
    </section>
    <section class="singleproduct-layout">
      <div class="container">
        <div class="row">
          <div class="col-md-4">
            <div class="sp-main">
              <h2 class="sp-title">{{ this.product.name }}</h2>
              <h4 class="sp-price">{{ this.productPrice }}</h4>
              <span class="sp-number">STYLE NUMBER: {{ this.product.model_no }}</span>
              <p>DETAILS</p>
              <div class="sp-list" v-html="this.product.description">
              </div>
              <p>COLOR</p>
              <ul class="product-color">
                <li v-for="(variation, index) in product.product_variation" :key="index">
                  <Swatch :variation="variation" :variationId="index"
                    v-on:changeFeatureImageOnClick="changeFeatureImageOnClick" />
                </li>
              </ul>
              <nuxt-link to="/" class="btn-print continue-btn">PRINT MY NAME</nuxt-link>
              <form class="sp-addbag">
                <h4>QUANTITY</h4>
                <input v-model="productQuanity" type="number" min="1">
                <button @click="addToBag()" type="button" class="continue-btn">ADD TO BAG</button>
                <button id="fav-sp" class="continue-btn">
                  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
                    <path
                      d="M462.3 62.6C407.5 15.9 326 24.3 275.7 76.2L256 96.5l-19.7-20.3C186.1 24.3 104.5 15.9 49.7 62.6c-62.8 53.6-66.1 149.8-9.9 207.9l193.5 199.8c12.5 12.9 32.8 12.9 45.3 0l193.5-199.8c56.3-58.1 53-154.3-9.8-207.9z" />
                  </svg>
                </button>
              </form>
            </div>
          </div>
          <div class="col-md-8">
            <div class="sp-slider">
              <DetailSlider v-if="renderDetailSlider" :productImages="productImages"/>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import axios from 'axios';
import DetailSlider from '@/components/AppDetailSlider.vue'
import Swatch from '@/components/AppSwatch'
import Breadcrumbs from '@/components/Breadcrumbs'
export default {
  components: {
    Breadcrumbs,
    Swatch,
    DetailSlider,
  },
  data() {
    return {
      productId: '',
      product: '',
      productPrice: '',
      productImages: {},
      selectedImage: '',
      variationId: '', //this is not the real variation id but the indexing of api response
      baseURL: this.$axios.defaults.baseURL, // Base Url
      renderDetailSlider: true,

      // cart oriented data
      productQuanity: 1,
      productVariationId: '', //this is the actual product variation id
    }
  },
  mounted() {

    this.getProductId();  // Get product id from URL

    this.getProduct(this.productId);  // Get Product function hits axios for Product details api

  },
  methods: {
    getProductId() {
      let url = new URL(location.href)
      this.productId = url.searchParams.get("productId");
    },
    getProduct(productId) {
      axios.get(this.baseURL + 'api/singleProduct?productId=' + productId) //Single Product End point
        .then((response) => {
          this.product = response.data.data;
          this.productPrice = this.product.product_variation[0].formated_price;
          this.productImages = this.product.product_variation[0].product_images;
          this.selectedImage = this.product.product_variation[0].product_images[0].product_image;
          this.variationId = 0;
          this.productVariationId = this.product.product_variation[this.variationId].id // actual product variation id is assigned

        }).catch(() => 'Products not available') //in case no product Available

    },
    changeFeatureImageOnClick(payload) { //Swatch on click function
      this.variationId = payload.variation_id;
      this.productPrice = this.product.product_variation[this.variationId].formated_price;
      this.productImages = this.product.product_variation[this.variationId].product_images;
      this.selectedImage = this.product.product_variation[this.variationId].product_images[0].product_image;
      this.productVariationId = this.product.product_variation[this.variationId].id // actual product variation id is assigned
      this.productQuanity = 1

      this.forceRerender(); // this function flushed the Detail Slider Component and renders it again
    },

    async forceRerender() {  // Force Re-render function

      this.renderDetailSlider = false; // Remove MyComponent from the DOM

      await this.$nextTick(); // Wait for the change to get flushed to the DOM

      this.renderDetailSlider = true; // Add the component back in
    },

    addToBag() {
      let cartArr = []; //array where new cart data is pushed

      let cart = { // collected data
        quantity: this.productQuanity,
        product_id: this.productId,
        product_variation_id: this.productVariationId
      }

      if (localStorage.getItem("cart") === null) { //if local stoage is does not contain cart data
        cartArr.push(cart);
        localStorage.setItem('cart', JSON.stringify(cartArr))

      } else { // if local storage contains cart data
        var cartData = localStorage.getItem('cart')
        cartData = JSON.parse(cartData)

        if (cartData.find(o => o.product_id === cart.product_id) && cartData.find(o => o.product_variation_id === cart.product_variation_id)) { // if the product already exists in the cart
          let index = cartData.findIndex(o => o.product_id === cart.product_id) // index of product
          cartData.splice(index, 1); // removing the product object
          cartData.push(cart) // pushing the updated product data
        } else { //if the product is newly added
          cartData.push(cart)
        }
        localStorage.setItem('cart', JSON.stringify(cartData)) //cart data is updated
      }

    }

  }


}

</script>
