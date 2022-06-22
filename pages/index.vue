<template>
  <div>
    <section class="banner-section">
      <AppBanner />
      <!-- <Nuxt /> -->
    </section>

    <section class="about-section">
      <div class="container">
        <div class="main-box">
          <div class="row">
            <div class="col-lg-3 col-md-12 col-sm-12">
              <div class="left-img">
                <h2>FABULOUS GIFT</h2>
                <a href="#">VIEW</a>
                <img src="~/assets/images/homepagegiftsJan.jpg">
              </div>
            </div>
            <div class="col-lg-9 col-md-12 col-sm-12">
              <div class="about-img">
                <img src="~/assets/images/homepagegiftsJan22.jpg">
              </div>
            </div>
          </div>

        </div>
      </div>


    </section>

     <section class="shop-section">
      <div class="container">
        <div class="shop-box">
          <div class="row">
            <div class="col-lg-6 col-md-6 col-sm-12">
              <div class="box-shop1"> 
                <img src="~/assets/images/shop-for-him.jpg">
                <h2>Shop For Him</h2>
              </div>
            </div>
            <div class="col-lg-6 col-md-6 col-sm-12">
              <div class="box-shop2"> 
                <img src="~/assets/images/shop-for-her.jpg">
                <h2>Shop For Her</h2>
              </div>
            </div>
          </div>

        </div>
      </div>


    </section>
    <section class="instagram-section">
      <div class="container">
        <div class="main-insta">
          <h2>connect with us</h2>
          <img src="~/assets/images/timeline-logo.png">
          <img src="~/assets/images/instgram.png" class="insta-img">


        </div>

      </div>
    </section>
  </div>
</template>

<script>
  import AppBanner from "@/components/AppBanner"
  export default {
    components: {
      AppBanner,
      head() {
        return {
          title: "WELCOME TO MJJ",
          meta: [{
            hid: 'description',
            name: 'Description',
            content: 'This is an app'
          }]
        }
      }
    }

  }

</script>
