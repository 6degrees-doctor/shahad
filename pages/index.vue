<template>
  <div>

    <!--  bg -->
    <div class="hero py-5 ps-5 ">
      <h1 class="h1  text-light py-3"> Rate Your <br>Favorite Doctor - by 6degrees</h1>
      <div class="gap-2 d-grid col-2">
        <button class="btn btn-secondary border-0 text-light" type="button"> Review</button>
      </div>
    </div>
    <!-- End bg -->


    <!-- Search Bar  -->
    <div class="container">
      <div class="row py-4 search m-3 rounded">
        <h2 class="text-dark m-3"> Search for a doctor</h2>
        <hr>
        <div class="col-lg-3 col-md-12 col-sm-12 m-3 ">
          <input class="form-control " list="datalistOptions1" id="exampleDataList1" placeholder="Name of doctor..">
          <datalist id="datalistOptions1">
            <option value="Doctor1" />
            <option value="Doctor2" />
            <option value="Doctor3" />
            <option value="Doctor4" />
            <option value="Doctor5" />

          </datalist>
        </div>
        <div class="col-lg-3 col-md-12 col-sm-12 m-3 ">
          <input class="form-control" list="datalistOptions2" id="exampleDataList2" placeholder="Select Department..">
          <datalist id="datalistOptions2">
            <option value="Doctor1"></option>
            <option value="Doctor2"></option>
            <option value="Doctor3"></option>
            <option value="Doctor4"></option>
            <option value="Doctor5"></option>
          </datalist>
        </div>
        <div class="col-lg-3 col-md-12 col-sm-12 m-3">
          <input class="form-control" list="datalistOptions3" id="exampleDataList3" placeholder="Select specialty..">
          <datalist id="datalistOptions3">
            <option value="Doctor1"></option>
            <option value="Doctor2"></option>
            <option value="Doctor3"></option>
            <option value="Doctor4"></option>
            <option value="Doctor5"></option>
          </datalist>
        </div>
        <div class="col  d-grid gap-2 m-3">
          <button class="btn btn-secondary border-0 text-light"><i class="bi bi-search"></i> Search</button>
        </div>
      </div>
    </div>
    <!-- Search Bar -->


    <!-- Hero Section -->
    <section class=" text-center  " id="aboutus">
      <div class="row rowcolor ">
        <div class="col-lg-8 col-md-12 col-12 text-start ps-5 my-5">
          <h1> Why our website?</h1>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore
            magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
            consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla
            pariatur. Excepteur sint occaecat cupidatat non proident,
            <br>sunt in culpa qui officia deserunt mollit anim id est laborum
          </p>
        </div>
        <div class="col-lg-4 col-md-12 col-12 ps-lg-5 mt-md-5 ">
          <img src="~/assets/images/colimg.jpg" class="img-fluid colimg rounded">
        </div>
      </div>

    </section>

    <!-- End Hero Section -->



    <!-- Top rated section -->
    <h2 class="text-center m-5">Top rated</h2>
    <div class="container">
      <div class="row g-2  mt-5 mb-5 rowcolor  ">
        <div class="col-md-4  d-flex justify-content-around">
          <div class="card p-3 text-start px-4 border-0 shadow">

            <img src="~/assets/images/doc1.jpg" class="card-img-top  img-fluid " style="width: 17rem;">


            <div class="card-body">

              <div class="card-title star">
                <i class="bi bi-star-fill"></i>
                <i class="bi bi-star-fill"></i>
                <i class="bi bi-star-fill"></i>
                <i class="bi bi-star-fill"></i>
                <i class="bi bi-star"></i>
                <span class="text-dark">40</span>
              </div>
              <h5 class="mb-0">Dr.Mai Hardy</h5>
              <p class="card-text">Internal Medicine</p>
            </div>



          </div>
        </div>

        <div class="col-md-4  d-flex justify-content-around">

          <div class="card p-3 text-start px-4  border-0 shadow">

            <img src="~/assets/images/doc2.jpg" class="card-img-top  img-fluid " style="width: 17rem;">


            <div class="card-body">

              <div class="card-title star">
                <i class="bi bi-star-fill"></i>
                <i class="bi bi-star-fill"></i>
                <i class="bi bi-star-fill"></i>
                <i class="bi bi-star-fill"></i>
                <i class="bi bi-star"></i>
                <span class="text-dark">40</span>
              </div>
              <h5 class="mb-0">Dr.Mai Hardy</h5>
              <p class="card-text">Internal Medicine</p>
            </div>



          </div>

        </div>

        <div class="col-md-4  d-flex justify-content-around">

          <div class="card p-3 text-start px-4  border-0 shadow">

            <img src="~/assets/images/doc4.jpg" class="card-img-top img-fluid " style="width: 17rem;">


            <div class="card-body">

              <div class="card-title star">
                <i class="bi bi-star-fill"></i>
                <i class="bi bi-star-fill"></i>
                <i class="bi bi-star-fill"></i>
                <i class="bi bi-star-fill"></i>
                <i class="bi bi-star"></i>
                <span class="text-dark">40</span>
              </div>
              <h5 class="mb-0">Dr.Mai Hardy</h5>
              <p class="card-text">Internal Medicine</p>
            </div>



          </div>

        </div>


      </div>
    </div>
    <!-- End Top rated section -->

    <!-- Review list section -->
    <h2 class="text-center m-5"> Write a Review</h2>
    <div class="container">
      <div class="row g-2  mt-5 mb-5 rowcolor  ">
        <div class="col-md-4  d-flex justify-content-around">
          <div class="card p-3 text-start px-4  border-0 shadow">

            <img src="~/assets/images/doc2.jpg" class="card-img-top  img-fluid " style="width: 17rem;">


            <div class="card-body">

              <div class="card-title star">
                <i class="bi bi-star-fill"></i>
                <i class="bi bi-star-fill"></i>
                <i class="bi bi-star-fill"></i>
                <i class="bi bi-star-fill"></i>
                <i class="bi bi-star"></i>
                <span class="text-dark">40</span>
              </div>
              <h5 class="mb-0">Dr.Mai Hardy</h5>
              <p class="card-text">Internal Medicine</p>
              <NuxtLink to="reviewpage"> <button class=" btn btn-secondary  border-0  text-light">Write a Review</button>
              </NuxtLink>
            </div>



          </div>
        </div>

        <div class="col-md-4  d-flex justify-content-around">

          <div class="card p-3 text-start px-4  border-0 shadow">

            <img src="~/assets/images/doc5.jpg" class="card-img-top  img-fluid " style="width: 17rem;">


            <div class="card-body">

              <div class="card-title star">
                <i class="bi bi-star-fill"></i>
                <i class="bi bi-star-fill"></i>
                <i class="bi bi-star-fill"></i>
                <i class="bi bi-star-fill"></i>
                <i class="bi bi-star"></i>
                <span class="text-dark">40</span>
              </div>
              <h5 class="mb-0">Dr.Mai Hardy</h5>
              <p class="card-text">Internal Medicine</p>
              <NuxtLink to="reviewpage"> <button class=" btn btn-secondary  border-0 text-light">Write a Review</button>
              </NuxtLink>
            </div>



          </div>

        </div>

        <div class="col-md-4  d-flex justify-content-around">

          <div class="card p-3 text-start px-4  border-0 shadow">

            <img src="~/assets/images/doc1.jpg" class="card-img-top  img-fluid  " style="width: 17rem;">


            <div class="card-body">

              <div class="card-title star">
                <i class="bi bi-star-fill"></i>
                <i class="bi bi-star-fill"></i>
                <i class="bi bi-star-fill"></i>
                <i class="bi bi-star-fill"></i>
                <i class="bi bi-star"></i>
                <span class="text-dark">40</span>
              </div>
              <h5 class="mb-0">Dr.Mai Hardy</h5>
              <p class="card-text">Internal Medicine</p>
              <NuxtLink to="reviewpage"> <button class="btn btn-secondary  border-0  text-light">Write a Review</button>
              </NuxtLink>
            </div>



          </div>

        </div>





      </div>
    </div>
    <!-- End Review list section -->



    <div class="   text-center p-5 rowcolor shadow">
      <h1 class=""><b> Contact us now!</b></h1>
      <p> Fell free to contact us at any time and we will respond to you soon.</p>
      <div class="container">
        <div class="row g-3 justify-content-center ">
          <div class="col-lg-4 col-12 d-grid gap-2">

            <NuxtLink to="contact"><button type="submit"
                class="btn btn-secondary border-0 shadow p-2 ps-5 px-5">Contact</button></NuxtLink>
          </div>

        </div>

      </div>

    </div>


  </div>
</template>

<script>
export default {

}
</script>

<style>
.hero {
  background-image: linear-gradient(0deg, #000000 -26.28%, rgba(54, 54, 54, 0) 100%), url("~/assets/images/background2.jpg");
  height: 500px;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;


}

.h1 {
  text-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
  font-size: 60px;
}

@media (min-width: 992px),
(min-width: 1200px) {
  .search {
    box-sizing: border-box;
    background: #ffffff;
    border: 1px solid #9b9999;
    box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.07);
    -ms-transform: translateX(-10%) translateY(-10%);
    -webkit-transform: translate(-50%, -50%);
    transform: translate(0%, -70%);

  }
}

.colimg {
  width: 17rem;
  filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.25));
}
</style>