<template>
  <div>
    <section class="breadcrumbs">
      <Breadcrumbs />
      <Nuxt />
    </section>
    <section class="account-login">
      <div class="container">
        <div class="row">
          <div class="col-md-4">
            <div class="account-box">
              <img src="~/assets/images/corporate-icon-1.png">
              <h3>My Account</h3>
              <p><nuxt-link to="#">Edit your account information
                Change your password
                Modify your address book entries
                Wish List</nuxt-link></p>

            </div>
          </div>
          <div class="col-md-4">
            <div class="account-box">
              <img src="~/assets/images/corporate-icon-2.png">
              <h3>My Orders</h3>
              <p> <nuxt-link to="#"> View your order history</nuxt-link></p>
            </div>
          </div>
          <div class="col-md-4">
            <div class="account-box">
              <img src="~/assets/images/corporate-icon-3.png">
              <h3>My Newsletter</h3>
              <p><nuxt-link to="#">Subscription</nuxt-link></p>

            </div>
          </div>
        </div>
      </div>


    </section>
  </div>
</template>
