<template>
  <div>
    <section v-if="banners" class="banner-section">
      <AppBanner :banners='banners' />
      <!-- <Nuxt /> -->
    </section>

    <section v-if="this.collections > 0" class="about-section">
      <div class="container">
        <div class="main-box">
          <h2>FABULOUS Gifts</h2>
          <div class="row">
            <div v-if="this.collectionImage1" class="col-md-4 left-img">
              <img :src="collectionImage1">
            </div>
            <div class="col-md-8">
              <div class="about-img">
                <div class="row">
                  <div v-if="this.collectionImage2" class="col-md-12">
                    <img :src="collectionImage2">
                  </div>
                  <div v-if="this.collectionImage3" class="col-md-6">
                    <img :src="collectionImage3">
                  </div>
                  <div v-if="this.collectionImage4" class="col-md-6">
                    <img :src="collectionImage4">
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section v-if="this.promotions > 0" class="shop-section">
      <div class="container">
        <div class="row">
          <div class="col-md-6 p-0">
            <div class="box-shop1 m-same img-hover-zoom">
              <img :src="promotionImage1">
              <h2>{{ promotionTitle1 }}</h2>
            </div>
          </div>
          <div class="col-md-6 p-0">
            <div class="box-shop2 m-same img-hover-zoom">
              <img :src="promotionImage2">
              <h2>{{ promotionTitle2 }}</h2>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section v-if="this.instagram > 0" class="instagram-section">
      <div class="container">
        <div class="main-insta">
          <h2>connect with us</h2>
          <img src="~/assets/images/instgram.png" class="insta-img">
        </div>
        <div class="main-insta">
          <a :href=this.instagramPost1.permalink target="_blank">
            <img :src="this.instagramPost1.media_url" style="width:20%;">
          </a>
          <!-- <h2>{{ instagramPost1.id }}</h2> -->
        </div>
        <div class="main-insta">
          <a :href=this.instagramPost2.permalink target="_blank">
            <img :src="this.instagramPost2.media_url" style="width:20%;">
          </a>
          <!-- <h2>{{ instagramPost2.id }}</h2> -->
        </div>
        <div class="main-insta">
          <a :href=this.instagramPost3.permalink target="_blank">
            <img :src="this.instagramPost3.media_url" style="width:20%;">
          </a>
          <!-- <h2>{{ instagramPost3.id }}</h2> -->
        </div>
        <div class="main-insta">
          <a :href=this.instagramPost4.permalink target="_blank">
            <img :src="this.instagramPost4.media_url" style="width:20%;">
          </a>
          <!-- <h2>{{ instagramPost4.id }}</h2> -->
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import axios from 'axios'
import AppBanner from "@/components/AppBanner"
export default {
  name: 'IndexComponent',

  components: {
    AppBanner,
  },
  data() {
    return {
      categories: {},
      banners: {},
      collections: {},
      promotions: {},
      instagram_access_token: '',
      instagram: {},
      baseURL: this.$axios.defaults.baseURL, // Base Url

      // Collecrtions data
      collectionImage1: '',
      collectionImage2: '',
      collectionImage3: '',
      collectionImage4: '',

      // Promotion Data
      promotionImage1: '',
      promotionTitle1: '',

      promotionImage2: '',
      promotionTitle2: '',

      // Instagram Data
      instagramPost1: {},
      instagramPost2: {},
      instagramPost3: {},
      instagramPost4: {},

    }
  },

  mounted() {
    this.getHomeEssentials() //  Get Banners Function
  },

  methods: {

    getHomeEssentials() { // Axios for getting Home Essentials

      // Main Api of Home
      axios.get(this.baseURL + 'api/main')
        .then((response) => {
          console.log('hala', response.data.data);
          this.categories = response.data.data.category
          this.banners = response.data.data.banners
          this.collections = response.data.data.collections
          this.promotions = response.data.data.promotions
          this.instagram_access_token = response.data.data.instagram[0].access_token ?? ''

          //Declaring Collections
          this.collectionImage1 = this.baseURL + 'storage/' + this.collections[0].image
          this.collectionImage2 = this.baseURL + 'storage/' + this.collections[1].image
          this.collectionImage3 = this.baseURL + 'storage/' + this.collections[2].image
          this.collectionImage4 = this.baseURL + 'storage/' + this.collections[3].image

          // Declaring Promotions
          this.promotionImage1 = this.baseURL + 'storage/' + this.promotions[0].image
          this.promotionTitle1 = this.promotions[0].title

          this.promotionImage2 = this.baseURL + 'storage/' + this.promotions[1].image
          this.promotionTitle2 = this.promotions[1].title
        }).then(() => { //Instagram basic display api request

          axios.get('https://graph.instagram.com/me/media?fields=id,media_url,media_type,username,timestamp,permalink&access_token=' + this.instagram_access_token)
            .then((response) => { //Assigning instagram response
              this.instagram = response.data.data
              this.instagramPost1 = this.instagram[0]
              this.instagramPost2 = this.instagram[1]
              this.instagramPost3 = this.instagram[2]
              this.instagramPost4 = this.instagram[3]
            }).catch(() => 'Something is wrong with the Instagram Access token') //in case token gets expired

        }).catch(() => 'Data not available') //in case admin has not uploaded images
    }
  }
}
</script>
