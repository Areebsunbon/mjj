<template>
  <div>
    <Breadcrumbs />
    <section class="checkout-page form-input">
      <div class="container">
        <form>
          <div class="checkout-layout">
            <div class="row">
              <div class="col-md-6">
                  <div class="payment-tab">
                    <i> <img src="~/assets/images/book-solid.svg"></i>
                    <h3>Payment details</h3>
                  </div>
                <div class="checkout-leftbar">
                  <div class="form-group">
                    <label class="col-form-label">NAME</label>
                    <div class="col-form-input">
                      <input type="text" class="form-control" id="first-name" placeholder="Name">
                    </div>
                  </div>
                  <div class="form-group">
                    <label class="col-form-label">TELEPHONE</label>
                    <div class="col-form-input">
                      <input type="number" class="form-control" id="exampleFormControlInput1" placeholder="Telephone">
                    </div>
                  </div>
                  <div class="form-group">
                    <label class="col-form-label">ADDRESS</label>
                    <div class="col-form-input">
                      <input type="text" class="form-control" id="exampleFormControlInput1" placeholder="ADDRESS">
                    </div>
                  </div>
                  <div class="checkout-location">
                    <div class="form-group">
                      <label class="col-form-label">COUNTRY</label>
                      <div class="col-form-input">
                        <select class="form-control" id="exampleFormControlSelect1">
                          <option>Pakistan</option>

                        </select>
                      </div>
                    </div>
                    <div class="form-group">
                      <label class="col-form-label">CITY</label>
                      <div class="col-form-input">
                        <select class="form-control" id="exampleFormControlSelect1">
                          <option>Karachi</option>
                          <option>Attock</option>
                          <option>Peshawar</option>

                        </select>
                      </div>
                    </div>


                  </div>


                </div>
                <div class="checkbox-checkout">
                  <div class="form-group form-check">
                    <input type="checkbox" class="form-check-input" id="exampleCheck1">
                    <label class="form-check-label" for="exampleCheck1">Create Account</label>
                  </div>
                  <div class="form-group form-check">
                    <input type="checkbox" class="form-check-input" id="exampleCheck1">
                    <label class="form-check-label" for="exampleCheck1">MY DELIVERY AND BILLING ADDRESSES ARE THE
                      SAME</label>
                  </div>
                  <div class="form-group form-check">
                    <input type="checkbox" class="form-check-input" id="exampleCheck1">
                    <label class="form-check-label" for="exampleCheck1">MY BILLING AND SHIPPING ADDRESSES ARE THE
                      SAME</label>
                  </div>

                </div>

              </div>

            </div>

          </div>
        </form>

      </div>
    </section>
  </div>
</template>
