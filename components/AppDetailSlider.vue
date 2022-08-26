<template>
  <div id="carouselExampleIndicators" class="carousel slide" data-ride="carousel">
    <ol class="carousel-indicators">
      <li v-for="(productImage, index) in productImages" data-target="#carouselExampleIndicators"
        :class="{ 'active': index == 0 }" :data-slide-to=index :key="index">
        <img @click="changeDisplayImage(index)" :src="productImage.product_image" class="d-block w-100">
      </li>
    </ol>
    <div class="carousel-inner">
      <div v-for="(productImage, index) in productImages" class="carousel-item" :class="{ 'active': index == 0 }"
        :key="index">
        <img :src="productImage.product_image" class="d-block w-100" />
      </div>
    </div>
    <button class="carousel-control-prev" type="button" data-target="#carouselExampleIndicators" data-slide="prev">
      <span class="carousel-control-prev-icon" aria-hidden="true"><svg xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 320 512">
          <path
            d="M34.52 239.03L228.87 44.69c9.37-9.37 24.57-9.37 33.94 0l22.67 22.67c9.36 9.36 9.37 24.52.04 33.9L131.49 256l154.02 154.75c9.34 9.38 9.32 24.54-.04 33.9l-22.67 22.67c-9.37 9.37-24.57 9.37-33.94 0L34.52 272.97c-9.37-9.37-9.37-24.57 0-33.94z" />
        </svg></span>
      <span class="sr-only">Previous</span>
    </button>
    <button class="carousel-control-next" type="button" data-target="#carouselExampleIndicators" data-slide="next">
      <span class="carousel-control-next-icon" aria-hidden="true"><svg xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 320 512">
          <path
            d="M285.476 272.971L91.132 467.314c-9.373 9.373-24.569 9.373-33.941 0l-22.667-22.667c-9.357-9.357-9.375-24.522-.04-33.901L188.505 256 34.484 101.255c-9.335-9.379-9.317-24.544.04-33.901l22.667-22.667c9.373-9.373 24.569-9.373 33.941 0L285.475 239.03c9.373 9.372 9.373 24.568.001 33.941z" />
        </svg></span>
      <span class="sr-only">Next</span>
    </button>
  </div>
</template>

<script>
export default {
  data() {
    return {
    }
  },
  props: [
    'productImages',
  ],
  methods: {
    changeDisplayImage(imageIndex) { // small inage on click function
      this.selectedImage = this.productImages[imageIndex].product_image;
    },
  },

}
</script>

<style>
</style>
