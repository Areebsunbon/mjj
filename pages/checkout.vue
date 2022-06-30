<template>
  <div>
    <Breadcrumbs />
    <section class="checkout-page form-input">
      <div class="container">
        <form>
          <div class="checkout-layout">
            <div class="row">
              <div class="col-md-5">
                <div class="checkout-bar">
                  <div class="payment-tab">
                    <i> <img src="~/assets/images/book-solid.svg"></i>
                    <h3>Payment details</h3>
                  </div>
                  <div class="checkout-leftbar">
                    <div class="form-group row">
                      <label class="col-lg-3 col-form-label">NAME</label>
                      <div class="col-lg-9 col-form-input">
                        <input type="text" class="form-control" id="first-name" placeholder="Name">
                      </div>
                    </div>
                    <div class="form-group row">
                      <label class="col-lg-3 col-form-label">TELEPHONE</label>
                      <div class="col-lg-9 col-form-input">
                        <input type="number" class="form-control" id="exampleFormControlInput1" placeholder="Telephone">
                      </div>
                    </div>
                    <div class="form-group row">
                      <label class="col-lg-3 col-form-label">ADDRESS</label>
                      <div class="col-lg-9 col-form-input">
                        <textarea class="form-control" rows="3" placeholder="ADDRESS"></textarea>
                      </div>
                    </div>
                    <div class="checkout-location">
                      <div class="form-group row">
                        <label class="col-lg-3 col-form-label">COUNTRY</label>
                        <div class="col-lg-9">
                            <div class="row">
                                <div class="col-lg-5">
                                    <select class="form-control" id="exampleFormControlSelect1">
                                        <option>Pakistan</option>
                                    </select>
                                </div>
                                <div class="col-lg-7">
                                    <div class="city-box">
                                        <label class="col-form-label">CITY</label>
                                        <div class="city-select">
                                        <select class="form-control" id="exampleFormControlSelect1">
                                            <option>Karachi</option>
                                            <option>Attock</option>
                                            <option>Peshawar</option>
                                        </select>
                                        </div>
                                    </div>
                                    

                                </div>
                         

                            </div>


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
                      <input type="checkbox" class="form-check-input" id="exampleCheck2">
                      <label class="form-check-label" for="exampleCheck2">My Delivery and Billing Address Are
                        Same</label>
                    </div>
                    <div class="form-group form-check">
                      <input type="checkbox" class="form-check-input" id="exampleCheck3">
                      <label class="form-check-label" for="exampleCheck3">Newsletter Subscribe</label>
                      </div>

                  </div>
                </div>
                <div class="checkout-bar">
                  <div class="payment-tab">
                    <i> <img src="~/assets/images/copy-regular.svg"></i>
                    <h3>Delivery Details</h3>
                  </div>
                  <div class="checkout-leftbar">
                    <div class="form-group row">
                      <label class="col-lg-3 col-form-label">NAME</label>
                      <div class="col-lg-9 col-form-input">
                        <input type="text" class="form-control" id="first-name" placeholder="Name">
                      </div>
                    </div>
                    <div class="form-group row">
                      <label class="col-lg-3 col-form-label">TELEPHONE</label>
                      <div class="col-lg-9 col-form-input">
                        <input type="number" class="form-control" id="exampleFormControlInput1" placeholder="Telephone">
                      </div>
                    </div>
                    <div class="form-group row">
                      <label class="col-lg-3 col-form-label">ADDRESS</label>
                      <div class="col-lg-9 col-form-input">
                        <textarea class="form-control" rows="3" placeholder="ADDRESS"></textarea>
                      </div>
                    </div>
                     <div class="checkout-location">
                      <div class="form-group row">
                        <label class="col-lg-3 col-form-label">COUNTRY</label>
                        <div class="col-lg-9">
                            <div class="row">
                                <div class="col-lg-5">
                                    <select class="form-control" id="exampleFormControlSelect1">
                                        <option>Pakistan</option>
                                    </select>
                                </div>
                                <div class="col-lg-7">
                                    <div class="city-box">
                                        <label class="col-form-label">CITY</label>
                                        <div class="city-select">
                                        <select class="form-control" id="exampleFormControlSelect1">
                                            <option>Karachi</option>
                                            <option>Attock</option>
                                            <option>Peshawar</option>
                                        </select>
                                        </div>
                                    </div>
                                    

                                </div>
                         

                            </div>


                        </div>
                        
                      </div>
                      
                    </div>
                  </div>

                </div>

              </div>

              <div class="col-md-7">
                <div class="row">
                  <div class="col-md-6">
                    <div class="checkout-bar">
                      <div class="payment-tab">
                        <i> <img src="~/assets/images/book-solid.svg"></i>
                        <h3>Shipping Method</h3>
                      </div>
                      <div class="checkout-leftbar right-layout">
                        <div class="form-check">
                          <input class="form-check-input" type="radio" name="exampleRadios" id="exampleRadios1"
                            value="option1" checked>
                          <label class="form-check-label" for="exampleRadios1">
                            Free Shipping
                          </label>
                        </div>
                      </div>

                    </div>

                  </div>
                  <div class="col-md-6">
                    <div class="checkout-bar">
                      <div class="payment-tab">
                        <i> <img src="~/assets/images/book-solid.svg"></i>
                        <h3>Payment Method</h3>
                      </div>
                      <div class="checkout-leftbar right-layout">
                        <div class="form-check">
                          <input class="form-check-input" type="radio" name="exampleRadios" id="exampleRadios2"
                            value="option1" checked>
                          <label class="form-check-label" for="exampleRadios2">
                            Cash on Delivery
                          </label>
                        </div>
                        <div class="form-check">
                          <input class="form-check-input" type="radio" name="exampleRadios" id="exampleRadios3"
                            value="option1" checked>
                          <label class="form-check-label" for="exampleRadios3">
                            Credit Card / Debit card
                          </label>
                        </div>
                        <div class="form-check">
                          <input class="form-check-input" type="radio" name="exampleRadios" id="exampleRadios4"
                            value="option1" checked>
                          <label class="form-check-label" for="exampleRadios4">
                            Bank Transfer
                          </label>
                        </div>
                      </div>
                    </div>
                  </div>
                  <div class="col-md-12">
                    <div class="checkout-bar">
                      <div class="payment-tab">
                        <i> <img src="~/assets/images/shopping-cart-solid.svg"></i>
                        <h3>Shipping Cart (0.25kg)</h3>
                      </div>
                      <div class="checkout-leftbar right-layout">
                          <div class="table-responsive">
                            <table class="table table-bordered">
                            <thead>
                                <tr>
                                <th scope="col">Image:</th>
                                <th scope="col">Product Name:</th>
                                <th scope="col">Quantity:</th>
                                <th scope="col">Unit Price:</th>
                                <th scope="col">Total:</th>
                                </tr>
                            </thead>
                            <tbody>
                                <tr>
                                <th><img src="~/assets/images/arrival.jpg"></th>
                                <td>
                                    <ul>
                                        <li>Button up Bi-Fold Wallet</li>
                                        <li>Color: Red</li>
                                        <li>
                                            <div class="table-edit">
                                                <li>PERSONALIZATION</li>
                                                <li><nuxt-link to="/">Edit Here</nuxt-link></li>
                                            </div>
                                        </li>
                                        <li>Text: Ahmed Mansoor</li>
                                        <li>Font: Font-38</li>
                                        <li>Color: Gold</li>
                                        <li>Placement: Outside</li>
                                    </ul>
                                </td>
                                <td class="btn-quantity">
                                    <div class="input-group">
                                        <span class="input-group-btn">
                                            <button type="button" class="quantity-left-minus btn"  data-type="minus" data-field="">
                                            <img src="~/assets/images/angle-down-solid.svg">
                                            </button>
                                        </span>
                                        <input type="text" id="quantity" name="quantity" class="form-control input-number" value="10" min="1" max="100">
                                        <span class="input-group-btn">
                                            <button type="button" class="quantity-right-plus btn" data-type="plus" data-field="">
                                                <img src="~/assets/images/angle-up-solid.svg">
                                            </button>
                                        </span>
                                        <span class="input-group-btn close-btn">
                                            <button type="button" class="quantity-close btn" data-type="plus" data-field="">
                                                <img src="~/assets/images/cancel.svg">
                                            </button>
                                        </span>
                                    </div>
                                </td>
                                <td>RS. 2,750</td>
                                <td>RS. 5,500</td>
                                </tr>
                                
                                
                            </tbody>
                            </table>
                         </div>
                        <div class="coupon-area">
                            <h3>Use Coupon Code</h3>
                            <div>
                                <input type="number" placeholder="Use Coupon Code">
                                <button type="submit" class="tick-coupon btn">
                                    <img src="~/assets/images/angle-up-solid.svg">
                                </button>
                            </div>

                        </div>
                        <div class="amount-area">
                            <ul>
                                <li>
                                    <span>Sub Total</span>
                                    <span>RS. 5,500</span>
                                </li>
                                <li>
                                    <span>Free Shipping</span>
                                    <span>RS. 0</span>
                                </li>
                                <li class="total-amount">
                                    <span> Total</span>
                                    <span>RS. 5,500</span>
                                </li>
                            </ul>

                        </div>

                      </div>
                    </div>
                  </div>
                  <div class="col-md-12">
                    <div class="checkout-bar">
                      <div class="checkout-leftbar right-layout">
                        <div class="message-area">
                            <label>Add Comment About Your Order</label>
                            <textarea class="form-control" rows="3"></textarea>
                        
                            <div class="form-check">
                                <input type="checkbox" class="form-check-input" id="exampleCheck8">
                                <label class="form-check-label" for="exampleCheck8">I Have Read And Agree To The Terms & Conditions</label>
                            </div>
                        </div>
                        <button type="submit" class="btn-confirm btn">Confirm Order</button>
                      </div>
                    </div>
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

// <script>
//   export default {
//     head() {
//       return {
//         script: [{
//           src: 'http://ajax.googleapis.com/ajax/libs/jquery/1.7.1/jquery.min.js'
//         }],
//       }
//     },

//   };
//   $(document).ready(function(){

// var quantitiy=0;
//   $('.quantity-right-plus').click(function(e){
        
//         // Stop acting like a button
//         e.preventDefault();
//         // Get the field name
//         var quantity = parseInt($('#quantity').val());
        
//         // If is not undefined
            
//             $('#quantity').val(quantity + 1);

          
//             // Increment
        
//     });

//      $('.quantity-left-minus').click(function(e){
//         // Stop acting like a button
//         e.preventDefault();
//         // Get the field name
//         var quantity = parseInt($('#quantity').val());
        
//         // If is not undefined
      
//             // Increment
//             if(quantity>0){
//             jQuery('#quantity').val(quantity - 1);
//             }
//     });
    
// });

// </script>
