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
                  <Product :product="product" />
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
import Product from '@/components/AppProduct'
import Breadcrumbs from '@/components/Breadcrumbs'
export default {
  components: {
    Breadcrumbs,
    Sidebar,
    Product,
  },
  data() {
    return {
      slug: '',
      products: {},
      baseURL: this.$axios.defaults.baseURL, // Base Url
      // featureImage: {}

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
          this.products = response.data.data;
          // this.featureImage = this.products.data[0].productimages.Feature[0].product_image

        }).catch(() => 'Products not available') //in case no product Available
    },

  }

}

</script>
