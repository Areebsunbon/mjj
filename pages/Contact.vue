<template>
  <div>
    <Breadcrumbs />
    <section class="contactus-layout form-input">
      <div class="container">
        <div class="contact-form">
          <div class="row">
            <div class="col-md-3">
              <div class="nav flex-column nav-pills" id="v-pills-tab" role="tablist" aria-orientation="vertical">
                <a class="nav-link active" id="v-pills-home-tab" data-toggle="pill" href="#v-pills-home" role="tab"
                  aria-controls="v-pills-home" aria-selected="true">get in touch</a>
                <a class="nav-link" id="v-pills-profile-tab" data-toggle="pill" href="#v-pills-profile" role="tab"
                  aria-controls="v-pills-profile" aria-selected="false">corporate inquires</a>
                <a class="nav-link" id="v-pills-messages-tab"  href="locator">Store Locator</a>

              </div>
            </div>
            <div class="col-md-9">
              <div class="tab-content" id="v-pills-tabContent">
                <div class="tab-pane fade show active" id="v-pills-home" role="tabpanel"
                  aria-labelledby="v-pills-home-tab">
                  <h4>GET IN TOUCH</h4>
                  <form>
                    <div class="form-fields">
                      <div class="form-group">
                        <input type="text" class="form-control" id="first-name" placeholder="First Name">
                        <input type="email" class="form-control" id="exampleFormControlInput1" placeholder="E-Mail">
                        <input type="number" class="form-control" id="exampleFormControlInput1" placeholder="Telephone">
                        <textarea class="form-control" id="exampleFormControlTextarea1" rows="5"
                          placeholder="Inquiry"></textarea>
                      </div>
                      <div class="btn-submit">
                        <button type="submit" class="btn btn-primary">Continue</button>
                      </div>
                    </div>

                  </form>

                </div>
                <div class="tab-pane fade" id="v-pills-profile" role="tabpanel" aria-labelledby="v-pills-profile-tab">
                  <h4>CORPORATE INQUIRIES</h4>
                  <div class="inquiries">
                    <p class="main-boxpara">The perfect way to show your appreciation! Handcrafted, personalized leather products! You can
                      personalize with your name, monogram, logo or a combination for a personal touch.</p>
                    <div class="row">
                      <div class="col-md-12 inquiries-box">
                        <nuxt-link to="#">
                          <div class="image-box">
                            <img src="~/assets/images/coporate-1.jpg" class="img-zoombox">
                            <div class="image-box-content">
                              <h3>YOUR LOGO</h3>
                              <p>Add your own custom or company logo with either our blind embossing or with our silver
                                and
                                gold foiling technique</p>
                            </div>
                          </div>
                        </nuxt-link>
                      </div>
                      <div class="col-md-12 inquiries-box">
                        <nuxt-link to="#">
                          <div class="image-box">
                            <img src="~/assets/images/coporate-2.jpg" class="img-zoombox">
                            <div class="image-box-content">
                              <h3>YOUR MONOGRAM</h3>
                              <p>Add your own monogram with either our blind embossing or with our silver and gold
                                foiling technique</p>
                            </div>
                          </div>
                        </nuxt-link>
                      </div>
                      <div class="col-md-12 inquiries-box">
                        <nuxt-link to="#">
                          <div class="image-box">
                            <img src="~/assets/images/coporate-3.jpg" class="img-zoombox">
                            <div class="image-box-content">
                              <h3>YOUR PACKAGING</h3>
                              <p> Your order will arrive in our signature MJ gift boxing, adorned with our signature
                                wrapping paper. </p>
                            </div>
                          </div>
                        </nuxt-link>
                      </div>
                      <div class="col-md-12 further-area">
                        <h3>FOR FURTHER INQUIRIES</h3>
                        <nuxt-link to="#">CONTACT US</nuxt-link>


                      </div>
                    </div>
                  </div>
                </div>
                <div class="tab-pane fade" id="v-pills-messages" role="tabpanel" aria-labelledby="v-pills-messages-tab">
                  ...</div>

              </div>
            </div>
          </div>


        </div>
      </div>
    </section>
  </div>
</template>
