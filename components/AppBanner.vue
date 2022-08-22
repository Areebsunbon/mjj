<template>
  <section class="banner-section">
    <div class="banner-full">
      <!-- if banners are provided by the admin -->
      <div id="carouselExampleCaptions" class="carousel slide" data-ride="carousel">
        <ol class="carousel-indicators">
          <li v-for="(banner, index) in banners" data-target="#carouselExampleCaptions"
            :class="{ 'active': index == 0 }" :data-slide-to=index :key="index"></li>
        </ol>
        <div class="carousel-inner">
          <div v-for="(banner, index) in banners" class="carousel-item" :class="{ 'active': index == 0 }" :key="index">
            <img :src="banner.banner_image" class="d-block w-100">
            <div class="carousel-caption">
              <h5>{{ banner.obj_value }}</h5>
              <p>{{ banner.description }}</p>
              <nuxt-link to="product">{{ banner.title }}</nuxt-link>
            </div>
          </div>
        </div>
      </div>
      <!-- else static banners are set -->

      <div class="overlay"></div>

    </div>
  </section>

</template>
<script>

export default {
  name : 'BannerComponenet',
  props: [
    'banners'
  ],

  // data() {
  //   return {
  //     banners: {},
  //     collections: {},
  //     baseURL: this.$axios.defaults.baseURL, // Base Url
  //   }
  // },

  // mounted() {
  //   this.getBanners() //  Get Banners Function
  // },

  // methods: {

  //   async getBanners() { // Axios for getting banners
  //     await axios.get(this.baseURL + 'api/main')
  //       .then((response) => {
  //         console.log(response.data);
  //         this.banners = response.data.data.banners
  //         this.collections = response.data.data.collections
  //       })
  //   }
  // }

}



</script>
