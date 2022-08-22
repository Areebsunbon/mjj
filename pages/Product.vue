<template>
  <div>
    <section class="breadcrumbs">
      <Breadcrumbs />
      <Nuxt />
    </section>
    <section class="product-layout">
      <div class="container">
        <div class="row">
          <div class="col-lg-2 col-md-3 col-sm-12">
            <Sidebar />

          </div>
          <div class="col-lg-10 col-md-9 col-sm-12">
            <div class="product-listing">
              <div class="row">
                <div class="col-12 product-category">
                  <h2>{{ this.slug }}</h2>
                </div>
                <div v-for="(product, productIndex) in products.data" class="col-4" :key="productIndex">
                  <div class="product-card">
                    <img :src="featureImage">
                    <div class="fav-icon">
                      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
                        <!-- Font Awesome Pro 5.15.4 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) -->
                        <path
                          d="M462.3 62.6C407.5 15.9 326 24.3 275.7 76.2L256 96.5l-19.7-20.3C186.1 24.3 104.5 15.9 49.7 62.6c-62.8 53.6-66.1 149.8-9.9 207.9l193.5 199.8c12.5 12.9 32.8 12.9 45.3 0l193.5-199.8c56.3-58.1 53-154.3-9.8-207.9z" />
                      </svg>
                    </div>
                    <ul v-for="(variation, index) in product.product_variation" class="product-color" :key="index">

                      <div v-if="variation.color_options.hex_value.length == 1"
                        v-on:mouseover="changeFeature(productIndex, index)" class="color-swatch m-auto S-20"
                        :style="{ 'background-color': variation.color_options.hex_value[0] }"></div>

                      <div v-if="variation.color_options.hex_value.length == 2"
                        v-on:mouseover="changeFeature(productIndex, index)" class="color-swatch m-auto S-20"
                        style="background-color:#eb0a0a ">
                        <div class="combination-swatch " style="background-color:#000000"></div>
                      </div>

                      <!-- <div
                         class="color-swatch m-auto S-20"
                        style="background-color:#eb0a0a ">
                        <div class="combination-swatch " style="background-color:#000000"></div>
                      </div>

                      <div v-if="variation.color_options.hex_value.length == 3" v-on:mouseover="changeFeature(productIndex, index)" class="color-swatch m-auto S-20" style="background-color:#eb0a0a ">
                        <div class="combination-swatch " style="background-color:#000000"></div>
                        <div class="combination-swatch swatch3" style="background-color:#ffae00"></div>
                      </div> -->



                      <!-- <li @click="changeFeature(productIndex, index)"
                        v-if="variation.color_options.hex_value.length > 1">
                        <div class="singleSwatch" v-for="(color, index) in variation.color_options.hex_value"
                          :style="{ 'background-color': variation.color_options.hex_value[1] }" :key="index"></div>
                      </li> -->
                      <!-- <li @click="changeFeature(productIndex, index)" v-else>
                        <div class="singleSwatch" :style="{ 'background-color': variation.color_options.hex_value[0] }">
                        </div>
                      </li> -->
                    </ul>
                    <h2>{{ product.name }}</h2>
                    <span>{{ product.price }}</span>
                  </div>

                </div>

              </div>

            </div>

          </div>

        </div>

      </div>

    </section>
  </div>
</template>

<script>
import axios from 'axios'
import Sidebar from '@/components/Sidebar'
import Breadcrumbs from '@/components/Breadcrumbs'
export default {
  components: {
    Breadcrumbs,
    Sidebar
  },
  data() {
    return {
      slug: '',
      products: {},
      baseURL: this.$axios.defaults.baseURL, // Base Url
      featureImage: {}

    }
  },
  mounted() {

    this.getSlug();  // Get Slug from URL

    this.getProducts();  // Get Prdocuts function hits axios for subCategory  api

  },

  methods: {
    getSlug() {
      let url = new URL(location.href)
      this.slug = url.searchParams.get("slug");
    },
    getProducts() {
      axios.get(this.baseURL + 'api/productsList?slug=' + this.slug) //subCategory End point
        .then((response) => {
          console.log('hala', response.data.data);
          this.products = response.data.data;
          this.featureImage = this.products.data[0].productimages.Feature[0].product_image

        }).catch(() => 'Products not available') //in case no product Available
    },
    changeFeature(productIndex, index) {
      this.featureImage = this.products.data[productIndex].productimages.Feature[index].product_image
    }
  }

}

</script>
