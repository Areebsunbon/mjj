<template>
  <div>
    <Breadcrumbs />
    <section class="register-page form-input">
      <div class="container">
        <div class="register-form">

          <div class="detail-form">
            <h2>Register Account</h2>
            <h4>Your Personal Details</h4>
            <form>
              <div class="form-group row">
                <label class="col-sm-2 col-form-label">NAME</label>
                <div class="col-sm-10">
                  <input type="text" class="form-control" id="first-name" placeholder="Name">
                </div>
              </div>
              <div class="form-group row">
                <label for="exampleFormControlInput1" class="col-sm-2 col-form-label">E-MAIL</label>
                <div class="col-sm-10">
                  <input type="email" class="form-control" id="exampleFormControlInput1" placeholder="E-Mail">
                </div>
              </div>
              <div class="form-group row">
                <label class="col-sm-2 col-form-label">TELEPHONE</label>
                <div class="col-sm-10">
                  <input type="number" class="form-control" id="exampleFormControlInput1" placeholder="Telephone">
                </div>
              </div>


              <h4>Your Password</h4>
              <div class="form-group row">
                <label for="inputPassword" class="col-sm-2 col-form-label">Password</label>
                <div class="col-sm-10">
                  <input type="password" class="form-control" id="inputPassword" placeholder="Password">
                </div>
              </div>
              <div class="form-group row">
                <label for="inputPassword" class="col-sm-2 col-form-label">CONFIRM PASSWORD</label>
                <div class="col-sm-10">
                  <input type="password" class="form-control" id="inputPassword" placeholder="Confirm Password">
                </div>
              </div>
              <h4>Newsletter</h4>
              <div class="form-group row subscribe-form">
                <div class="col-sm-2">
                  <label for="inputPassword" class="col-form-label">SUBSCRIBE TO NEWSLETTER</label>
                </div>
                <div class="col-sm-10 btn-radio">
                  <div class="form-check">
                    <input class="form-check-input" type="radio" name="gridRadios" id="gridRadios1" value="option1"
                      checked>
                    <label class="form-check-label" for="gridRadios1">
                      YES
                    </label>
                  </div>
                  <div class="form-check">
                    <input class="form-check-input" type="radio" name="gridRadios" id="gridRadios2" value="option2">
                    <label class="form-check-label" for="gridRadios2">
                      NO
                    </label>
                  </div>
                </div>

              </div>
              <div class="form-group submit-area">
                <div class="policy-area">
                    <label class="form-check-label" for="gridCheck1">
                    I have read and agree to the Privacy Policy
                  </label>
                  <input class="form-check-input" type="checkbox" id="gridCheck1">
                  
                </div>
                <div class="btn-submit">
                  <button type="submit" class="btn btn-primary">Continue</button>
                </div>

              </div>



            </form>

          </div>

        </div>

      </div>
    </section>
  </div>
</template>
