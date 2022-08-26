<template>
  <div>
    <!-- NORMAL SCREEN START -->
    <div class="container-fluid">
      <div class="normal-header">
        <div class="header-middle">
          <div class="header-search">
            <ul>
              <li>
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512">
                  <!--! Font Awesome Pro 6.1.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
                  <path
                    d="M549.655 124.083c-6.281-23.65-24.787-42.276-48.284-48.597C458.781 64 288 64 288 64S117.22 64 74.629 75.486c-23.497 6.322-42.003 24.947-48.284 48.597-11.412 42.867-11.412 132.305-11.412 132.305s0 89.438 11.412 132.305c6.281 23.65 24.787 41.5 48.284 47.821C117.22 448 288 448 288 448s170.78 0 213.371-11.486c23.497-6.321 42.003-24.171 48.284-47.821 11.412-42.867 11.412-132.305 11.412-132.305s0-89.438-11.412-132.305zm-317.51 213.508V175.185l142.739 81.205-142.739 81.201z" />
                </svg>
              </li>
              <li>
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 320 512">
                  <!--! Font Awesome Pro 6.1.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
                  <path
                    d="M279.14 288l14.22-92.66h-88.91v-60.13c0-25.35 12.42-50.06 52.24-50.06h40.42V6.26S260.43 0 225.36 0c-73.22 0-121.08 44.38-121.08 124.72v70.62H22.89V288h81.39v224h100.17V288z" />
                </svg>
              </li>
              <li>
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
                  <!--! Font Awesome Pro 6.1.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
                  <path
                    d="M459.37 151.716c.325 4.548.325 9.097.325 13.645 0 138.72-105.583 298.558-298.558 298.558-59.452 0-114.68-17.219-161.137-47.106 8.447.974 16.568 1.299 25.34 1.299 49.055 0 94.213-16.568 130.274-44.832-46.132-.975-84.792-31.188-98.112-72.772 6.498.974 12.995 1.624 19.818 1.624 9.421 0 18.843-1.3 27.614-3.573-48.081-9.747-84.143-51.98-84.143-102.985v-1.299c13.969 7.797 30.214 12.67 47.431 13.319-28.264-18.843-46.781-51.005-46.781-87.391 0-19.492 5.197-37.36 14.294-52.954 51.655 63.675 129.3 105.258 216.365 109.807-1.624-7.797-2.599-15.918-2.599-24.04 0-57.828 46.782-104.934 104.934-104.934 30.213 0 57.502 12.67 76.67 33.137 23.715-4.548 46.456-13.32 66.599-25.34-7.798 24.366-24.366 44.833-46.132 57.827 21.117-2.273 41.584-8.122 60.426-16.243-14.292 20.791-32.161 39.308-52.628 54.253z" />
                </svg>
              </li>
              <li>
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512">
                  <!--! Font Awesome Pro 6.1.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
                  <path
                    d="M224.1 141c-63.6 0-114.9 51.3-114.9 114.9s51.3 114.9 114.9 114.9S339 319.5 339 255.9 287.7 141 224.1 141zm0 189.6c-41.1 0-74.7-33.5-74.7-74.7s33.5-74.7 74.7-74.7 74.7 33.5 74.7 74.7-33.6 74.7-74.7 74.7zm146.4-194.3c0 14.9-12 26.8-26.8 26.8-14.9 0-26.8-12-26.8-26.8s12-26.8 26.8-26.8 26.8 12 26.8 26.8zm76.1 27.2c-1.7-35.9-9.9-67.7-36.2-93.9-26.2-26.2-58-34.4-93.9-36.2-37-2.1-147.9-2.1-184.9 0-35.8 1.7-67.6 9.9-93.9 36.1s-34.4 58-36.2 93.9c-2.1 37-2.1 147.9 0 184.9 1.7 35.9 9.9 67.7 36.2 93.9s58 34.4 93.9 36.2c37 2.1 147.9 2.1 184.9 0 35.9-1.7 67.7-9.9 93.9-36.2 26.2-26.2 34.4-58 36.2-93.9 2.1-37 2.1-147.8 0-184.8zM398.8 388c-7.8 19.6-22.9 34.7-42.6 42.6-29.5 11.7-99.5 9-132.1 9s-102.7 2.6-132.1-9c-19.6-7.8-34.7-22.9-42.6-42.6-11.7-29.5-9-99.5-9-132.1s-2.6-102.7 9-132.1c7.8-19.6 22.9-34.7 42.6-42.6 29.5-11.7 99.5-9 132.1-9s102.7-2.6 132.1 9c19.6 7.8 34.7 22.9 42.6 42.6 11.7 29.5 9 99.5 9 132.1s2.7 102.7-9 132.1z" />
                </svg>
              </li>
            </ul>
            <div class="search-form">
              <form>
                <div class="input-group">
                  <div class="form-outline">
                    <input type="search" id="form1" class="form-control" />
                  </div>
                  <button type="button" class="btn btn-primary">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
                      <!--! Font Awesome Pro 6.1.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
                      <path
                        d="M500.3 443.7l-119.7-119.7c27.22-40.41 40.65-90.9 33.46-144.7C401.8 87.79 326.8 13.32 235.2 1.723C99.01-15.51-15.51 99.01 1.724 235.2c11.6 91.64 86.08 166.7 177.6 178.9c53.8 7.189 104.3-6.236 144.7-33.46l119.7 119.7c15.62 15.62 40.95 15.62 56.57 0C515.9 484.7 515.9 459.3 500.3 443.7zM79.1 208c0-70.58 57.42-128 128-128s128 57.42 128 128c0 70.58-57.42 128-128 128S79.1 278.6 79.1 208z" />
                    </svg>
                  </button>
                </div>
              </form>
            </div>
          </div>
          <div class="header-code">
            <p>10% OFF ON ENTIRE ONLINE STORE PROMOCODE: MJ22</p>
          </div>
          <div class="right-menu">
            <ul>
              <li class="nav-item dropdown">
                    <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button"
                      data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                      <strong>Rs</strong> Currency
                    </a>
                    <div class="dropdown-menu" aria-labelledby="navbarDropdown">
                    <ul>
                      <li><nuxt-link to="/"> Euror</nuxt-link>
                    </li>
                    <li>
                    <nuxt-link to="/"> Pakistan</nuxt-link></li>
                     <li>
                    <nuxt-link to="/"> Dollar</nuxt-link></li>
                    </ul>
                    </div>
                  </li>
              <li>
                <nuxt-link to="/" data-toggle="modal" data-target="#exampleModalCenter">
                  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512">
                    <!--! Font Awesome Pro 6.1.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
                    <path
                      d="M224 256c70.7 0 128-57.31 128-128s-57.3-128-128-128C153.3 0 96 57.31 96 128S153.3 256 224 256zM274.7 304H173.3C77.61 304 0 381.6 0 477.3c0 19.14 15.52 34.67 34.66 34.67h378.7C432.5 512 448 496.5 448 477.3C448 381.6 370.4 304 274.7 304z" />
                  </svg>
                  MY BAGS <span>(0)</span></nuxt-link>
              </li>
              <div class="modal fade" id="exampleModalCenter" tabindex="-1" role="dialog"
                aria-labelledby="exampleModalCenterTitle" aria-hidden="true">
                <div class="modal-dialog modal-dialog-centered modal-dialog-scrollable" role="document">
                  <div class="modal-content">
                    <div class="modal-header">
                      <h5 class="modal-title" id="exampleModalLongTitle">MY BAG</h5>
                      <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                        <span aria-hidden="true">&times;</span>
                      </button>
                    </div>
                    <div class="modal-body">
                      <div class="bag-modal">
                        <div class="product-bag">
                          <img src="~/assets/images/popup.jpg">
                          <div class="product-detail-modal">
                            <h2>2 PC His & Her Gift Set</h2>
                            <p>Rs.6,000</p>
                            <span> Style Number: MJGS06</span>
                            <ul>
                              <li>Color: red</li>
                              <li>QTY: x1 | <nuxt-link to="/">Remove</nuxt-link>
                              </li>
                            </ul>
                          </div>
                        </div>
                      </div>
                    </div>
                    <div class="modal-footer">
                      <div class="modal-p-price">
                        <ul>
                          <li><strong>SUB-TOTAL</strong> RS.6,000</li>
                          <li><strong>FREE SHIPPING</strong> RS.0</li>
                          <li><strong>TOTAL </strong> RS.6,000</li>
                        </ul>
                        <div class="btn-checkout">
                          <button type="button" class="btn btn-continue" data-dismiss="modal">Continue Shopping</button>
                          <button type="button" class="btn btn-continue">Checkout</button>

                        </div>
                      </div>

                    </div>
                  </div>
                </div>
              </div>
               <li class="nav-item dropdown">
                    <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button"
                      data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                      My Account
                    </a>
                    <div class="dropdown-menu" aria-labelledby="navbarDropdown">
                    <ul>
                      <li><nuxt-link to="register"> Register</nuxt-link>
                    </li>
                    <li>
                    <nuxt-link to="login"> Login</nuxt-link></li>
                    </ul>
                     

                    </div>
                  </li>


            </ul>

          </div>
        </div>
        <div class="header-end">
          <div class="header-inner">

            <div class="row mb-0">
              <div class="col-12">
                <nuxt-link to="/"><img src="~/assets/images/mjjlogo.svg"></nuxt-link>

              </div>
              <div class="col-12">
                <ul class="navbar">
                  <li class="nav-item dropdown">
                    <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button"
                      data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                      Women
                    </a>
                    <div class="dropdown-menu" aria-labelledby="navbarDropdown">
                      <nuxt-link to="/" class="dropdown-item">Handbags </nuxt-link>
                      <nuxt-link to="/" class="dropdown-item">Document Cases</nuxt-link>
                      <nuxt-link to="/" class="dropdown-item"> Wallets</nuxt-link>
                      <nuxt-link to="/" class="dropdown-item">Card Cases</nuxt-link>
                      <nuxt-link to="/" class="dropdown-item"> Accessories</nuxt-link>
                      <nuxt-link to="/" class="dropdown-item">Travel</nuxt-link>
                      <nuxt-link to="/" class="dropdown-item">Fashion Show</nuxt-link>

                    </div>
                  </li>
                 <li class="nav-item dropdown">
                    <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button"
                      data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                      Men
                    </a>
                    <div class="dropdown-menu" aria-labelledby="navbarDropdown">
                      <nuxt-link to="/" class="dropdown-item">Document Cases </nuxt-link>
                      <nuxt-link to="/" class="dropdown-item"> Wallets</nuxt-link>
                      <nuxt-link to="/" class="dropdown-item">Card Cases</nuxt-link>
                      <nuxt-link to="/" class="dropdown-item"> Accessories</nuxt-link>
                      <nuxt-link to="/" class="dropdown-item">Travel</nuxt-link>
                      <nuxt-link to="/" class="dropdown-item">Fashion Show</nuxt-link>

                    </div>
                  </li>
                  <li class="nav-item dropdown">
                    <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button"
                      data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                      Travel
                    </a>
                    <div class="dropdown-menu" aria-labelledby="navbarDropdown">
                      <nuxt-link to="/" class="dropdown-item">Travel Bags / Trolleys </nuxt-link>
                      <nuxt-link to="/" class="dropdown-item">Toiletry Cases</nuxt-link>
                      <nuxt-link to="/" class="dropdown-item">  Passport holders</nuxt-link>
                    </div>
                  </li>
                  <li class="nav-item dropdown">
                    <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button"
                      data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                      Office
                    </a>
                    <div class="dropdown-menu" aria-labelledby="navbarDropdown">
                      <nuxt-link to="/" class="dropdown-item">Portfolios / Folders</nuxt-link>
                      <nuxt-link to="/" class="dropdown-item">Office Desk Accessories</nuxt-link>
                    </div>
                  </li>
                  <li class="nav-item dropdown">
                    <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button"
                      data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                     Gifts
                    </a>
                    <div class="dropdown-menu" aria-labelledby="navbarDropdown">
                      <nuxt-link to="/" class="dropdown-item">Gift Sets</nuxt-link>
                      <nuxt-link to="/" class="dropdown-item"> Photo Frames</nuxt-link>
                      <nuxt-link to="/" class="dropdown-item"> Accessories</nuxt-link>
                      <nuxt-link to="/" class="dropdown-item"> Buy A Gift Voucher</nuxt-link>
                    </div>
                  </li> 
                  <li class="nav-item dropdown">
                    <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button"
                      data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                     The House of MJ
                    </a>
                    <div class="dropdown-menu" aria-labelledby="navbarDropdown">
                      <nuxt-link to="/" class="dropdown-item">History</nuxt-link>
                      <nuxt-link to="/" class="dropdown-item">YouTube Videos</nuxt-link>
                      <nuxt-link to="/" class="dropdown-item">Fashion shows</nuxt-link>
                       <nuxt-link to="/" class="dropdown-item">Story</nuxt-link>
                    </div>
                  </li>

                  <!-- <div class="sub-menu">
                    <div class="container">
                      <div class="row">
                        <div class="col-3">
                          <ul class="dropdown">
                            <li>
                              <h2> Bags</h2>
                              <nuxt-link to="/">Handbags </nuxt-link>
                              <nuxt-link to="/">Document Cases</nuxt-link>
                              <nuxt-link to="/"> Wallets</nuxt-link>
                              <nuxt-link to="/">Card Cases</nuxt-link>
                              <nuxt-link to="/"> Accessories</nuxt-link>
                              <nuxt-link to="/">Travel</nuxt-link>
                              <nuxt-link to="/">Fashion Show</nuxt-link>
                            </li>
                          </ul>
                        </div>
                        <div class="col-3">
                          <ul class="dropdown">
                            <li>
                              <h2> Small Leather Goods</h2>
                              <nuxt-link to="/">Small Wallets </nuxt-link>
                              <nuxt-link to="/">Continental Wallets</nuxt-link>
                              <nuxt-link to="/">Key Rings & Holders</nuxt-link>
                              <nuxt-link to="/">Card Cases</nuxt-link>
                            </li>
                          </ul>
                        </div>
                        <div class="col-3">
                          <ul class="dropdown">
                            <li>
                              <h2> Accessories</h2>
                              <nuxt-link to="/">Jewelry Cases </nuxt-link>
                              <nuxt-link to="/">Watch Cases</nuxt-link>
                              <nuxt-link to="/">Accessories Boxes</nuxt-link>
                            </li>
                          </ul>
                        </div>
                        <div class="col-3">
                          <ul class="dropdown">
                            <li>
                              <h2> New Arrival</h2>
                              <img src="~/assets/images/arrival.jpg">

                            </li>
                          </ul>
                        </div>
                      </div>
                    </div>
                  </div> -->


                </ul>
              </div>
            </div>

          </div>
        </div>

      </div>
    </div>

    <!-- MOBILE HEADER START -->
    <div class="mobile-header">
      <div class="header-middle">
        <div class="header-inner">
          <div class="row mb-0 align-items-center">
            <div class="col-3">


              <!-- Toggler -->
              <button data-mdb-toggle="sidenav" data-mdb-target="#sidenav-1" class="btn btn-primary"
                aria-controls="#sidenav-1" aria-haspopup="true">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512">
                  <!-- Font Awesome Pro 5.15.4 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) -->
                  <path
                    d="M16 132h416c8.837 0 16-7.163 16-16V76c0-8.837-7.163-16-16-16H16C7.163 60 0 67.163 0 76v40c0 8.837 7.163 16 16 16zm0 160h416c8.837 0 16-7.163 16-16v-40c0-8.837-7.163-16-16-16H16c-8.837 0-16 7.163-16 16v40c0 8.837 7.163 16 16 16zm0 160h416c8.837 0 16-7.163 16-16v-40c0-8.837-7.163-16-16-16H16c-8.837 0-16 7.163-16 16v40c0 8.837 7.163 16 16 16z" />
                </svg>
              </button>
              <!-- Toggler -->
              <!-- Sidenav -->
              <nav id="sidenav-1" class="sidenav" data-mdb-hidden="false">
                <!-- <ul class="sidenav-menu">
                  <li class="sidenav-item">
                    <a class="sidenav-link">
                      <i class="far fa-smile fa-fw me-3"></i><span>Link 1</span></a>
                  </li>
                  <li class="sidenav-item">
                    <a class="sidenav-link"><i class="fas fa-grin fa-fw me-3"></i><span>Category 1</span></a>
                    <ul class="sidenav-collapse show">
                      <li class="sidenav-item">
                        <a class="sidenav-link">Link 2</a>
                      </li>
                      <li class="sidenav-item">
                        <a class="sidenav-link">Link 3</a>
                      </li>
                    </ul>
                  </li>
                  <li class="sidenav-item">
                    <a class="sidenav-link"><i class="fas fa-grin-wink fa-fw me-3"></i><span>Category
                        2</span></a>
                    <ul class="sidenav-collapse">
                      <li class="sidenav-item">
                        <a class="sidenav-link">Link 4</a>
                      </li>
                      <li class="sidenav-item">
                        <a class="sidenav-link">Link 5</a>
                      </li>
                    </ul>
                  </li>
                </ul> -->
                <ul class="sidenav-menu">
                  <li class="nav-item dropdown">
                    <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button"
                      data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                      Women
                    </a>
                    <div class="dropdown-menu" aria-labelledby="navbarDropdown">
                      <nuxt-link to="/" class="dropdown-item">Handbags </nuxt-link>
                      <nuxt-link to="/" class="dropdown-item">Document Cases</nuxt-link>
                      <nuxt-link to="/" class="dropdown-item"> Wallets</nuxt-link>
                      <nuxt-link to="/" class="dropdown-item">Card Cases</nuxt-link>
                      <nuxt-link to="/" class="dropdown-item"> Accessories</nuxt-link>
                      <nuxt-link to="/" class="dropdown-item">Travel</nuxt-link>
                      <nuxt-link to="/" class="dropdown-item">Fashion Show</nuxt-link>

                    </div>
                  </li>
                 <li class="nav-item dropdown">
                    <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button"
                      data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                      Men
                    </a>
                    <div class="dropdown-menu" aria-labelledby="navbarDropdown">
                      <nuxt-link to="/" class="dropdown-item">Document Cases </nuxt-link>
                      <nuxt-link to="/" class="dropdown-item"> Wallets</nuxt-link>
                      <nuxt-link to="/" class="dropdown-item">Card Cases</nuxt-link>
                      <nuxt-link to="/" class="dropdown-item"> Accessories</nuxt-link>
                      <nuxt-link to="/" class="dropdown-item">Travel</nuxt-link>
                      <nuxt-link to="/" class="dropdown-item">Fashion Show</nuxt-link>

                    </div>
                  </li>
                  <li class="nav-item dropdown">
                    <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button"
                      data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                      Travel
                    </a>
                    <div class="dropdown-menu" aria-labelledby="navbarDropdown">
                      <nuxt-link to="/" class="dropdown-item">Travel Bags / Trolleys </nuxt-link>
                      <nuxt-link to="/" class="dropdown-item">Toiletry Cases</nuxt-link>
                      <nuxt-link to="/" class="dropdown-item">  Passport holders</nuxt-link>
                    </div>
                  </li>
                  <li class="nav-item dropdown">
                    <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button"
                      data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                      Office
                    </a>
                    <div class="dropdown-menu" aria-labelledby="navbarDropdown">
                      <nuxt-link to="/" class="dropdown-item">Portfolios / Folders</nuxt-link>
                      <nuxt-link to="/" class="dropdown-item">Office Desk Accessories</nuxt-link>
                    </div>
                  </li>
                  <li class="nav-item dropdown">
                    <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button"
                      data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                     Gifts
                    </a>
                    <div class="dropdown-menu" aria-labelledby="navbarDropdown">
                      <nuxt-link to="/" class="dropdown-item">Gift Sets</nuxt-link>
                      <nuxt-link to="/" class="dropdown-item"> Photo Frames</nuxt-link>
                      <nuxt-link to="/" class="dropdown-item"> Accessories</nuxt-link>
                      <nuxt-link to="/" class="dropdown-item"> Buy A Gift Voucher</nuxt-link>
                    </div>
                  </li> 
                  <li class="nav-item dropdown">
                    <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button"
                      data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                     The House of MJ
                    </a>
                    <div class="dropdown-menu" aria-labelledby="navbarDropdown">
                      <nuxt-link to="/" class="dropdown-item">History</nuxt-link>
                      <nuxt-link to="/" class="dropdown-item">YouTube Videos</nuxt-link>
                      <nuxt-link to="/" class="dropdown-item">Fashion shows</nuxt-link>
                       <nuxt-link to="/" class="dropdown-item">Story</nuxt-link>
                    </div>
                  </li>

                  <!-- <div class="sub-menu">
                    <div class="container">
                      <div class="row">
                        <div class="col-3">
                          <ul class="dropdown">
                            <li>
                              <h2> Bags</h2>
                              <nuxt-link to="/">Handbags </nuxt-link>
                              <nuxt-link to="/">Document Cases</nuxt-link>
                              <nuxt-link to="/"> Wallets</nuxt-link>
                              <nuxt-link to="/">Card Cases</nuxt-link>
                              <nuxt-link to="/"> Accessories</nuxt-link>
                              <nuxt-link to="/">Travel</nuxt-link>
                              <nuxt-link to="/">Fashion Show</nuxt-link>
                            </li>
                          </ul>
                        </div>
                        <div class="col-3">
                          <ul class="dropdown">
                            <li>
                              <h2> Small Leather Goods</h2>
                              <nuxt-link to="/">Small Wallets </nuxt-link>
                              <nuxt-link to="/">Continental Wallets</nuxt-link>
                              <nuxt-link to="/">Key Rings & Holders</nuxt-link>
                              <nuxt-link to="/">Card Cases</nuxt-link>
                            </li>
                          </ul>
                        </div>
                        <div class="col-3">
                          <ul class="dropdown">
                            <li>
                              <h2> Accessories</h2>
                              <nuxt-link to="/">Jewelry Cases </nuxt-link>
                              <nuxt-link to="/">Watch Cases</nuxt-link>
                              <nuxt-link to="/">Accessories Boxes</nuxt-link>
                            </li>
                          </ul>
                        </div>
                        <div class="col-3">
                          <ul class="dropdown">
                            <li>
                              <h2> New Arrival</h2>
                              <img src="~/assets/images/arrival.jpg">

                            </li>
                          </ul>
                        </div>
                      </div>
                    </div>
                  </div> -->


                </ul>
              </nav>
              <!-- Sidenav -->

            </div>
            <div class="col-6">
              <img src="~/assets/images/mjjlogo.svg">
            </div>
            <div class="col-3">
              <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512">
                <!-- Font Awesome Pro 5.15.4 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) -->
                <path
                  d="M352 160v-32C352 57.42 294.579 0 224 0 153.42 0 96 57.42 96 128v32H0v272c0 44.183 35.817 80 80 80h288c44.183 0 80-35.817 80-80V160h-96zm-192-32c0-35.29 28.71-64 64-64s64 28.71 64 64v32H160v-32zm160 120c-13.255 0-24-10.745-24-24s10.745-24 24-24 24 10.745 24 24-10.745 24-24 24zm-192 0c-13.255 0-24-10.745-24-24s10.745-24 24-24 24 10.745 24 24-10.745 24-24 24z" />
              </svg>

            </div>

          </div>
        </div>
      </div>

      <div class="header-end">
        <div class="container">
          <div class="row">
            <div class="col-12">
              <div class="header-search">
                <div class="search-form">
                  <form>
                    <div class="input-group">
                      <div class="form-outline">
                        <input type="search" id="form1" class="form-control" />
                      </div>
                      <button type="button" class="btn btn-primary">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
                          <!--! Font Awesome Pro 6.1.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
                          <path
                            d="M500.3 443.7l-119.7-119.7c27.22-40.41 40.65-90.9 33.46-144.7C401.8 87.79 326.8 13.32 235.2 1.723C99.01-15.51-15.51 99.01 1.724 235.2c11.6 91.64 86.08 166.7 177.6 178.9c53.8 7.189 104.3-6.236 144.7-33.46l119.7 119.7c15.62 15.62 40.95 15.62 56.57 0C515.9 484.7 515.9 459.3 500.3 443.7zM79.1 208c0-70.58 57.42-128 128-128s128 57.42 128 128c0 70.58-57.42 128-128 128S79.1 278.6 79.1 208z" />
                        </svg>
                      </button>
                    </div>
                  </form>
                </div>
              </div>
            </div>
            <div class="col-12">
              <div class="right-menu">
                <ul>
                  <li class="nav-item dropdown">
                    <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button"
                      data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                      My Account
                    </a>
                    <div class="dropdown-menu" aria-labelledby="navbarDropdown">
                    <ul>
                      <li><nuxt-link to="register"> Register</nuxt-link>
                    </li>
                    <li>
                    <nuxt-link to="login"> Login</nuxt-link></li>
                    </ul>
                    </div>
                  </li>
                  <!-- <li>
                    <select class="form-select" aria-label="Default select example">
                      <option selected><strong>Rs</strong> Currency</option>
                      <option value="1">Euro</option>
                      <option value="2">Pakistan</option>
                      <option value="3">Dollar</option>
                    </select>
                  </li> -->
                  <li class="nav-item dropdown">
                    <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button"
                      data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                      <strong>Rs</strong> Currency
                    </a>
                    <div class="dropdown-menu" aria-labelledby="navbarDropdown">
                    <ul>
                      <li><nuxt-link to="/"> Euror</nuxt-link>
                    </li>
                    <li>
                    <nuxt-link to="/"> Pakistan</nuxt-link></li>
                     <li>
                    <nuxt-link to="/"> Dollar</nuxt-link></li>
                    </ul>
                    </div>
                  </li>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

</template>

<script>
  export default {
    name: 'AppHeader'

  };

</script>
<style>
  .header {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

</style>
