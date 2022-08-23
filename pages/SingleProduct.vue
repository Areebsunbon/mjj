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
              <h4 class="sp-price">{{ this.product.formated_price }}</h4>
              <span class="sp-number">STYLE NUMBER: {{ this.product.model_no }}</span>
              <p>DETAILS</p>
              <div class="sp-list" v-html="this.product.description">
              </div>
              <p>COLOR</p>
              <ul class="product-color">
      <li v-for="(variation, index) in product.product_variation" :key="index">

        <Swatch :variation="variation" v-on:changeFeatureImage="changeFeatureImage(variation)" />

      </li>
    </ul>
              <nuxt-link to="/" class="btn-print continue-btn">PRINT MY NAME</nuxt-link>
              <form class="sp-addbag">
                <h4>QUANTITY</h4>
                <input type="number">
                <button type="submit" class="continue-btn">ADD TO BAG</button>
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
              <div id="carouselExampleIndicators" class="carousel slide" data-ride="carousel">
                <ol class="carousel-indicators">
                  <li data-target="#carouselExampleIndicators" data-slide-to="0" class="active"><img
                      src="~/assets/images/product1.jpg" class="d-block w-100"></li>
                  <li data-target="#carouselExampleIndicators" data-slide-to="1"><img src="~/assets/images/product2.jpg"
                      class="d-block w-100"></li>

                </ol>
                <div class="carousel-inner">
                  <div class="carousel-item active">
                    <img src="~/assets/images/product1.jpg" class="d-block w-100">
                  </div>
                  <div class="carousel-item">
                    <img src="~/assets/images/product2.jpg" class="d-block w-100">
                  </div>
                </div>
                <button class="carousel-control-prev" type="button" data-target="#carouselExampleIndicators"
                  data-slide="prev">
                  <span class="carousel-control-prev-icon" aria-hidden="true"><svg xmlns="http://www.w3.org/2000/svg"
                      viewBox="0 0 320 512">
                      <path
                        d="M34.52 239.03L228.87 44.69c9.37-9.37 24.57-9.37 33.94 0l22.67 22.67c9.36 9.36 9.37 24.52.04 33.9L131.49 256l154.02 154.75c9.34 9.38 9.32 24.54-.04 33.9l-22.67 22.67c-9.37 9.37-24.57 9.37-33.94 0L34.52 272.97c-9.37-9.37-9.37-24.57 0-33.94z" />
                    </svg></span>
                  <span class="sr-only">Previous</span>
                </button>
                <button class="carousel-control-next" type="button" data-target="#carouselExampleIndicators"
                  data-slide="next">
                  <span class="carousel-control-next-icon" aria-hidden="true"><svg xmlns="http://www.w3.org/2000/svg"
                      viewBox="0 0 320 512">
                      <path
                        d="M285.476 272.971L91.132 467.314c-9.373 9.373-24.569 9.373-33.941 0l-22.667-22.667c-9.357-9.357-9.375-24.522-.04-33.901L188.505 256 34.484 101.255c-9.335-9.379-9.317-24.544.04-33.901l22.667-22.667c9.373-9.373 24.569-9.373 33.941 0L285.475 239.03c9.373 9.372 9.373 24.568.001 33.941z" />
                    </svg></span>
                  <span class="sr-only">Next</span>
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import axios from 'axios';
import Swatch from '@/components/AppSwatch'
import Breadcrumbs from '@/components/Breadcrumbs'
export default {
  components: {
    Breadcrumbs,
    Swatch,
  },
  data() {
    return {
      productId: '',
      product: '',
      productPrice: '',
      baseURL: this.$axios.defaults.baseURL, // Base Url
    }
  },
  mounted() {

    this.getProductId();  // Get product id from URL

    this.getProduct(this.productId);  // Get Product function hits axios for Product details  api

  },
  methods: {
    getProductId() {
      let url = new URL(location.href)
      this.productId = url.searchParams.get("productId");
      // console.log('hala', this.productId);
    },
    getProduct(productId) {
      axios.get(this.baseURL + 'api/singleProduct?productId=' + productId) //Single Product End point
        .then((response) => {
          // console.log('hala',response);
          this.product = response.data.data;
        }).catch(() => 'Products not available') //in case no product Available
    },
    changeFeatureImage(variation){
      // alert('hala')
      console.log('hala',variation);
    }

  }


}

</script>
