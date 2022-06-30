<template>
  <section class="banner-section">
    <div class="banner-full">
      <div id="carouselExampleCaptions" class="carousel slide" data-ride="carousel">
        <ol class="carousel-indicators">
          <li data-target="#carouselExampleCaptions" data-slide-to="0" class="active"></li>
          <li data-target="#carouselExampleCaptions" data-slide-to="1"></li>
          <li data-target="#carouselExampleCaptions" data-slide-to="2"></li>
        </ol>
        <div class="carousel-inner">
          <div class="carousel-item active">
            <img src="~/assets/images/slide1.jpg" class="d-block w-100">
            <div class="carousel-caption">
              <h5>BE THE DIFFERENCE</h5>
              <p>Some representative placeholder content for the first slide.Some representative placeholder content for the first slide.</p>
               <nuxt-link to="#">View Product</nuxt-link>
            </div>
          </div>
          <div class="carousel-item">
             <img src="~/assets/images/slide2.png" class="d-block w-100">
            <div class="carousel-caption">
                <h5>BEAUTIFY THE ELEGANE</h5>
                 <p>Some representative placeholder content for the first slide.Some representative placeholder content for the first slide.</p>
              <nuxt-link to="#">View Product</nuxt-link>
            </div>
          </div>
          <div class="carousel-item">
            <img src="~/assets/images/slide4.jpg" class="d-block w-100">
            <div class="carousel-caption">
               <h5>BEAUTIFY THE ELEGANE</h5>
                <p>Some representative placeholder content for the first slide.Some representative placeholder content for the first slide.</p>
              <nuxt-link to="#">View Product</nuxt-link>
            </div>
          </div>
        </div>
        <!-- <button class="carousel-control-prev" type="button" data-target="#carouselExampleCaptions" data-slide="prev">
          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
          <span class="sr-only">Previous</span>
        </button>
        <button class="carousel-control-next" type="button" data-target="#carouselExampleCaptions" data-slide="next">
          <span class="carousel-control-next-icon" aria-hidden="true"></span>
          <span class="sr-only">Next</span>
        </button> -->
      </div>
      <div class="overlay"></div>
      <!-- <div id="carouselExampleControls" class="carousel slide" data-ride="carousel">
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
      </div> -->

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
    },

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
