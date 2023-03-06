<template>
  <div>

    <div class="container-fluid ">
      <div class="row bg ps-4 py-3">

        <div class="col d-flex ">
          <NuxtLink to="/" class=" text-decoration-none text-light">Home></NuxtLink>
          <NuxtLink to="reviewpage" class=" text-decoration-none text-light">Review</NuxtLink>
          <a class=" text-decoration-none text-dark ps-1" disabled>Active Page</a>
        </div>
      </div>
    </div>
    s
    <div class="container   shadow ">
      <div class="row rowcolor mt-5 rounded ">
        <div class="col-lg-4 col-md-12 col-12 ps-5 m-2">
          <img src="~/assets/images/doc2.jpg" class="img-fluid rounded-circle shadow imgd">
        </div>
        <div class="vr d-none d-sm-block" style="background-color: #48A2B1;"></div>
        <div class="col-lg-3 col-md-12 col-12 m-2 mt-5 ">
          <h5 class=""> <b>Dr. Mohammad Mazen</b> </h5>

          <div class="star">
            <i class="bi bi-star-fill"></i>
            <i class="bi bi-star-fill"></i>
            <i class="bi bi-star-fill"></i>
            <i class="bi bi-star-fill"></i>
            <i class="bi bi-star"></i>
          </div>
          <p class=""> Lorem ipsum dolor sit amet, consectetur adipiscing elit,
            occaecat cupidatat non proident. </p>
          <div class="col-lg-12 mt-3">
            <h6><b> Hospital:</b></h6>
            <p> King Fahad Hospital</p>
            <h6> <b>Specialty:</b></h6>
            <p> Dentist</p>
            <h6> <b>Department:</b></h6>
            <p> Dentist</p>
          </div>

          <div class="col-lg-12  col-sm-12">
            <h4><b>Pending Comments</b></h4> <!--This section only for authorized doctors  -->
            <div class="card" style="width: 35rem;">
              <div class="card-body">
                <p class="card-title"><b>Anonymous</b></p>
                <p class="card-subtitle mb-2 text-muted">18,March,2022</p>
                <div class="star">
                  <i class="bi bi-star-fill"></i>
                  <i class="bi bi-star-fill"></i>
                  <i class="bi bi-star-fill"></i>
                  <i class="bi bi-star-fill"></i>
                  <i class="bi bi-star"></i>
                </div>
                <p class="card-text">Lorem ipsum dolor sit amet, consectetur adipiscing elit . </p>
                <button href="#" class="btn btn-success  " style=""><i class="bi bi-check2 "></i></button>
                <button href="#" class="btn btn-danger"><i class="bi bi-x"></i></button>
              </div>
            </div>
            <div class="card" style="width: 35rem;">
              <div class="card-body">
                <p class="card-title"><b>Anonymous</b></p>
                <p class="card-subtitle mb-2 text-muted">18,March,2022</p>
                <div class="star">
                  <i class="bi bi-star-fill"></i>
                  <i class="bi bi-star-fill"></i>
                  <i class="bi bi-star-fill"></i>
                  <i class="bi bi-star-fill"></i>
                  <i class="bi bi-star"></i>
                </div>
                <p class="card-text">Lorem ipsum dolor sit amet, consectetur adipiscing elit . </p>
                <button href="#" class="btn btn-success"><i class="bi bi-check2 "></i></button>
                <button href="#" class="btn btn-danger"><i class="bi bi-x"></i></button>
              </div>
            </div>
          </div>
        </div>
      </div>


    </div>




    <div class="container">
      <div class="row rowcolor mt-5 ps-5 rounded  shadow py-5">
        <div class="col-lg-12 col-md-12 col-10  ">
          <h4 class="mt-4"> <i class="bi bi-pencil-square "></i><b>Write a Review</b></h4>
          <hr>
          <div class=" col-lg-4 col-md-12 col-12  mb-3">
            <label for="exampleFormControlInput1" class="form-label">Name:</label>
            <input type="email" class="form-control" id="exampleFormControlInput1" placeholder="Enter your name..">

          </div>
          <div class="col-lg-8 col-md-12 col-12 mb-3">
            <label for="exampleFormControlTextarea1" class="form-label">Comment:</label>
            <textarea class="form-control" id="exampleFormControlTextarea1" rows="5"
              placeholder="Write your comment.."></textarea>
          </div>
          <div class=" d-flex justify-content-start">
            <div class="d-grid gap-2 col-lg-2 col-12">
              <button class="btn btn-secondary  border-0 text-light">Send</button>
              <a href="" class="text-dark ps-3 mt-2 " data-bs-toggle="modal" data-bs-target="#exampleModal">Anonymous?</a>
            </div>
            <!-- Button trigger modal -->
            <!-- Modal -->
            <div class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel"
              aria-hidden="true">
              <div class="modal-dialog">
                <div class="modal-content">
                  <div class="modal-header">
                    <h1 class="modal-title fs-5" id="exampleModalLabel"><b>Anonymous</b> </h1>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                  </div>
                  <div class="modal-body">
                    <label for="exampleFormControlTextarea1" class="form-label">Comment:</label>
                    <textarea class="form-control" id="exampleFormControlTextarea2" rows="5"
                      placeholder="Write your comment.."></textarea>
                    <div class="col-md-12 col-md-12 col-12 d-grid gap-2  mt-4 ">
                      <button class="btn btn-secondary  border-0 text-light">Send</button>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>


    <div class="container shadow">
      <div class="row  rowcolor mt-5 ">
        <div class="row text-light ms-5 mt-3">
          <div class="col-lg-2 col-8 ps-5  rounded-2" style="background-color:#48A2B1;">
            <h2 class="mt-5"><b>4.7</b></h2>
            <div class="star">
              <i class="bi bi-star-fill"></i>
              <i class="bi bi-star-fill"></i>
              <i class="bi bi-star-fill"></i>
              <i class="bi bi-star-fill"></i>
              <i class="bi bi-star"></i>
            </div>
            <p> Based on reviews</p>
          </div>


          <div class="col-lg-8 col-8 m-3 d-grid gap-3  ">
            <div class="progress" style="background-color: #D9D9D9;">
              <div class="progress-bar" role="progressbar" aria-label="Basic example" aria-valuenow="0" aria-valuemin="0"
                aria-valuemax="100">
              </div>

            </div>
            <div class="progress " style="background-color: #D9D9D9;">
              <div class="progress-bar bg-warning" role="progressbar" aria-label="Success example" style="width: 25%"
                aria-valuenow="25" aria-valuemin="0" aria-valuemax="100">

              </div>
            </div>
            <div class="progress" style="background-color: #D9D9D9;">
              <div class="progress-bar bg-warning" role="progressbar" aria-label="Info example" style="width: 50%"
                aria-valuenow="50" aria-valuemin="0" aria-valuemax="100"></div>
            </div>
            <div class="progress" style="background-color: #D9D9D9;">
              <div class="progress-bar bg-warning" role="progressbar" aria-label="Warning example" style="width: 60%"
                aria-valuenow="60" aria-valuemin="0" aria-valuemax="100"></div>
            </div>
            <div class="progress" style="background-color: #D9D9D9;">
              <div class="progress-bar bg-warning" role="progressbar" aria-label="Danger example" style="width: 75%"
                aria-valuenow="75" aria-valuemin="0" aria-valuemax="100"></div>
            </div>

          </div>
        </div>

        <hr>
        <div class="col-md-10 col-12 mt-3">
          <div class="card">
            <div class="card-body ">
              <div class="row ">
                <div class="col-lg-2 col-12 d-flex justify-content-center align-items-center ">
                  <img src="~/assets/images/usericon.jpg" class="rounded-circle usericon img-fluid " />
                </div>
                <div class="col-lg-8 ">
                  <div class="star">
                    <i class="bi bi-star-fill"></i>
                    <i class="bi bi-star-fill"></i>
                    <i class="bi bi-star-fill"></i>
                    <i class="bi bi-star-fill"></i>
                    <i class="bi bi-star"></i>
                  </div>
                  <p class="fw-bold  text-muted mb-0">Sara - March 18, 2020</p>
                  <p class="text-muted fw-light mb-4">
                    Lorem ipsum dolor, sit amet consectetur adipisicing elit. Id quam sapiente
                    molestiae numquam quas, voluptates omnis nulla ea odio quia similique
                    corrupti magnam.
                  </p>
                </div>
              </div>
            </div>


          </div>
          <div class="card">
            <div class="card-body ">
              <div class="row ">
                <div class="col-lg-2 d-flex justify-content-center align-items-center mb-4 mb-lg-0">
                  <img src="~/assets/images/usericon.jpg" class="rounded-circle img-fluid usericon" />
                </div>
                <div class="col-lg-8 ">
                  <div class="star">
                    <i class="bi bi-star-fill"></i>
                    <i class="bi bi-star-fill"></i>
                    <i class="bi bi-star-fill"></i>
                    <i class="bi bi-star-fill"></i>
                    <i class="bi bi-star"></i>
                  </div>
                  <p class="fw-bold text-muted mb-0">Sara - March 18, 2020</p>
                  <p class="text-muted fw-light mb-4">
                    Lorem ipsum dolor, sit amet consectetur adipisicing elit. Id quam sapiente
                    molestiae numquam quas, voluptates omnis nulla ea odio quia similique
                    corrupti magnam.
                  </p>
                </div>
              </div>
            </div>


          </div>

          <div class="card">
            <div class="card-body ">
              <div class="row ">
                <div class="col-lg-2 d-flex justify-content-center align-items-center mb-4 mb-lg-0">
                  <img src="~/assets/images/usericon.jpg" class="rounded-circle img-fluid usericon" />
                </div>
                <div class="col-lg-8 ">
                  <div class="star">
                    <i class="bi bi-star-fill"></i>
                    <i class="bi bi-star-fill"></i>
                    <i class="bi bi-star-fill"></i>
                    <i class="bi bi-star-fill"></i>
                    <i class="bi bi-star"></i>
                  </div>
                  <p class="fw-bold text-muted mb-0">Sara - March 18, 2020</p>
                  <p class="text-muted fw-light mb-4">
                    Lorem ipsum dolor, sit amet consectetur adipisicing elit. Id quam sapiente
                    molestiae numquam quas, voluptates omnis nulla ea odio quia similique
                    corrupti magnam.
                  </p>
                </div>
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

}
</script>
<style>
.bg {
  background-color: #48A2B1;
}

.imgd {
  width: 300px;
}

.usericon {
  width: 80px;
}
</style>