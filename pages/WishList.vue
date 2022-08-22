<template>
  <div class="container">
    <section class="breadcrumbs">
      <Breadcrumbs />
      <Nuxt />
    </section>
    <section class="wish-list">
      <h2>My Wish List</h2>
      <div class="table-responsive">
        <table class="table table-bordered">
          <thead>
            <tr>
              <th scope="col"></th>
              <th scope="col">Product</th>
              <th scope="col">Style Number</th>
              <th scope="col">Availability</th>
              <th scope="col">Price</th>
              <th scope="col"></th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <th><img src="~/assets/images/arrival.jpg"></th>
              <td>
                <p>Continental Wallet with Mobile Pocket</p>
              </td>
              <td>
                <p>7374</p>
              </td>
              <td>
                <p>In Stock</p>
              </td>
              <td>
                <p>Rs.3,650</p>
              </td>
              <td>
                  <div class="wish-btn">
                       <nuxt-link to="#" class="btn-wish">
                  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512">
                    <path
                      d="M572.52 241.4C518.29 135.59 410.93 64 288 64S57.68 135.64 3.48 241.41a32.35 32.35 0 0 0 0 29.19C57.71 376.41 165.07 448 288 448s230.32-71.64 284.52-177.41a32.35 32.35 0 0 0 0-29.19zM288 400a144 144 0 1 1 144-144 143.93 143.93 0 0 1-144 144zm0-240a95.31 95.31 0 0 0-25.31 3.79 47.85 47.85 0 0 1-66.9 66.9A95.78 95.78 0 1 0 288 160z" />
                  </svg>
                </nuxt-link>
                <nuxt-link to="#" class="btn-wish">
                  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 352 512">
                    <path
                      d="M242.72 256l100.07-100.07c12.28-12.28 12.28-32.19 0-44.48l-22.24-22.24c-12.28-12.28-32.19-12.28-44.48 0L176 189.28 75.93 89.21c-12.28-12.28-32.19-12.28-44.48 0L9.21 111.45c-12.28 12.28-12.28 32.19 0 44.48L109.28 256 9.21 356.07c-12.28 12.28-12.28 32.19 0 44.48l22.24 22.24c12.28 12.28 32.2 12.28 44.48 0L176 322.72l100.07 100.07c12.28 12.28 32.2 12.28 44.48 0l22.24-22.24c12.28-12.28 12.28-32.19 0-44.48L242.72 256z" />
                    </svg>
                </nuxt-link>


                  </div>
               
              </td>
            </tr>
          </tbody>
        </table>
      </div>
      <div class="wish-continue">
          <a href="#" class="continue-btn">Continue</a>
      </div>
    </section>
  </div>
</template>
