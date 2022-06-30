<template>
  <div>
    <section class="banner-section">
      <AppBanner />
      <!-- <Nuxt /> -->
    </section>

    <section class="about-section">
      <div class="container">
        <div class="main-box">
          <h2>FABULOUS Gifts</h2>
          <div class="row">
            <div class="col-md-4 left-img">
                <img src="~/assets/images/fab1.png">
            </div>
            <div class="col-md-8">
              <div class="about-img">
                <div class="row">
                  <div class="col-md-12">
                    <img src="~/assets/images/fab2.png">
                  </div>
                  <div class="col-md-6">
                    <img src="~/assets/images/fab3.png">
                  </div>
                  <div class="col-md-6">
                    <img src="~/assets/images/fab4.png">
                  </div>
                </div>
                
              </div>
            </div>
          </div>

        </div>
      </div>


    </section>

     <section class="shop-section">
      <div class="container">
     
          <div class="row">
            <div class="col-md-6 p-0">
              <div class="box-shop1 m-same img-hover-zoom"> 
                <img src="~/assets/images/shop-for-him.jpg">
                <h2>Shop For Him</h2>
              </div>
            </div>
            <div class="col-md-6 p-0">
              <div class="box-shop2 m-same img-hover-zoom"> 
                <img src="~/assets/images/shop-for-her.jpg">
                <h2>Shop For Her</h2>
              </div>
            </div>
          </div>

        
      </div>


    </section>
    <section class="instagram-section">
      <div class="container">
        <div class="main-insta">
          <h2>connect with us</h2>
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
