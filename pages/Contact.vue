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
                <a class="nav-link" id="v-pills-messages-tab" data-toggle="pill" href="#v-pills-messages" role="tab"
                  aria-controls="v-pills-messages" aria-selected="false">Store Locator</a>
               
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
                  ...</div>
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
