<template>
  <div>
    <Breadcrumbs />
    <section class="login-page">
      <div class="container">
        <div class="row">
          <div class="col-md-6">
            <div class="login-card">
              <h2>New Customer</h2>
              <span>REGISTER</span>
              <p>By creating an account you will be able to shop faster, be up to date on an order's status, and keep
                track of the orders you have previously made.</p>
              <nuxt-link to="#">Continue</nuxt-link>
            </div>
          </div>
          <div class="col-md-6">
            <div class="login-card login-form">
              <h2>Returning Customer</h2>
              <span>SIGN IN</span>
              <form>
                <div class="form-group">
                  <label for="exampleInputEmail1">Email address</label>
                  <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="E-Mail">
                  
                </div>
                <div class="form-group">
                  <label for="exampleInputPassword1">Password</label>
                  <input type="password" class="form-control" id="exampleInputPassword1" placeholder="Password">
                  <nuxt-link to="#">Forgot Password</nuxt-link>
                </div>
               
                <button type="submit" class="btn btn-primary">Login</button>
              </form>
            </div>
          </div>
        </div>


      </div>
    </section>
  </div>
</template>
