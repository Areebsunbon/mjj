<template>

  <div class="product-card">
    <nuxt-link :to="'singleproduct?productId='+product.id">

      <img :src="featureImage">

    </nuxt-link>

    <div class="fav-icon">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
        <!-- Font Awesome Pro 5.15.4 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) -->
        <path
          d="M462.3 62.6C407.5 15.9 326 24.3 275.7 76.2L256 96.5l-19.7-20.3C186.1 24.3 104.5 15.9 49.7 62.6c-62.8 53.6-66.1 149.8-9.9 207.9l193.5 199.8c12.5 12.9 32.8 12.9 45.3 0l193.5-199.8c56.3-58.1 53-154.3-9.8-207.9z" />
      </svg>
    </div>
    <ul v-for="(variation, index) in product.product_variation" class="product-color" :key="index">

      <Swatch :variation="variation" v-on:changeFeatureImage="changeFeatureImage(variation)" />

    </ul>
    <h2>{{ product.name }}</h2>
    <span>{{ product.price }}</span>
  </div>


</template>

<script>
import Swatch from '@/components/AppSwatch'
export default {
  name: 'ProductComponenet',
  components: {
    Swatch
  },
  props: [
    'product'
  ],
  data() {
    return {
      featureImage: this.product.productimages.Feature[0].product_image
    }
  },
  methods: {
    changeFeatureImage(variation) {
      this.featureImage = variation.product_images[0].product_image
    },
  }
}
</script>

<style>
</style>
