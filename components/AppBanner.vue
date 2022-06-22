<template>
  <section class="banner-section">
    <div class="banner-full">
      <!-- <b-carousel id="carousel" v-model=" slide" :interval="3500" controls indicators
        style="text-shadow: 1px 1px 2px #333" @sliding-start="onSlideStart" @sliding-end="onSlideEnd">
        <div v-for="image in Images" :key="image.id">
          <div v-if="image.id <= 5">
           <b-carousel-slide :img-src="image.url"> </b-carousel-slide>
          </div>
        </div>
      </b-carousel> -->
      <div id="carouselExampleControls" class="carousel slide" data-ride="carousel">
        <div class="carousel-inner">
          <div class="carousel-item active">
            <img src="~/assets/images/slide1.jpg">
          </div>
          <div class="carousel-item">
            <img src="~/assets/images/slide2.jpg">
          </div>
          <div class="carousel-item">
            <img src="~/assets/images/slide3.jpg">
          </div>
        </div>
        <button class="carousel-control-prev" type="button" data-target="#carouselExampleControls" data-slide="prev">
          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
          <span class="sr-only">Previous</span>
        </button>
        <button class="carousel-control-next" type="button" data-target="#carouselExampleControls" data-slide="next">
          <span class="carousel-control-next-icon" aria-hidden="true"></span>
          <span class="sr-only">Next</span>
        </button>
      </div>

    </div>
  </section>

</template>
<script>
  export default {
    name: 'AppBanner',
    head() {
      return {
        script: [{
          src: 'https://cdn.jsdelivr.net/npm/bootstrap@4.6.1/dist/js/bootstrap.bundle.min.js'
        }],
      }
    }

  };



  //   import axios from 'axios'
  //   export default {
  //     data() {
  //       return {
  //         url: "",
  //         Images: [{


  //           },

  //         ],
  //         slide: 0,
  //         sliding: null
  //       }
  //     },
  //     method: {
  //       onSlideStart(slide) {
  //         this.sliding = true
  //       },
  //       onSlideEnd(slide) {
  //         this.sliding = false
  //       }
  //     },
  //     mounted() {
  //       console.log("hala");

  //       axios.get('http://3.135.102.9:9117/api/main').then((response) => {
  //         console.log(response.data.data.banners[0].banner_image);
  //         this.url = response.data.data.banners[0].banner_image;
  //       });
  //     },

  //     async asyncData() {

  //       try {
  //         let {
  //           data
  //         } = await axios.get('https://jsonplaceholder.typicode.com/photos')
  //         console.log(data,"datadata")
  //         return {
  //           Images: data
  //         }
  //       } catch (err) {
  //         console.log(err);

  //       }
  //     }


  //   }

</script>
