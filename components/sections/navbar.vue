<template>
  <div>

<nav class="navbar navbar-expand-lg bg-body-tertiary shadow">
  <div class="container-fluid  " >
    <img src="~/assets/images/logo.png" class="img-fluid" style="width: 8rem;" >
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span> 
    </button>
    <div class=" collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0 ">
        <li class="nav-item  ">
          
          <NuxtLink to="/" class="nav-link home ms-4 "><b>Home</b>
            </NuxtLink>
        </li>
        <li class="nav-item ">
          <a href="about" class="nav-link a ms-4">  About
          </a>
     </li>
        <li class="nav-item">
          <NuxtLink to="reviewpage" class="nav-link a ms-4" >Review
            </NuxtLink>
        </li>
        <li class="nav-item">
          <NuxtLink to="contact" class="nav-link a ms-4" >Contact
            </NuxtLink>
        </li>
      </ul>
      <span class="navbar-text">
      
  <div class="modal fade" id="exampleModalToggle" aria-hidden="true" aria-labelledby="exampleModalToggleLabel" tabindex="-1">
    <div class="modal-dialog modal-dialog-centered">
      <div class="modal-content">
        <div class="modal-header">
          <h1 class="modal-title fs-5 text-dark" id="exampleModalToggleLabel"><b>Sign in</b></h1>
          <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
        </div>
        <div class="modal-body">
          <form class="row g-3">
            <div class="col-md-12">
              <label class="text-dark">Username:</label>
              <input type="text" class="form-control" id="validationDefault01" placeholder="Enter Your Username" required>
            </div>
            <div class="col-md-12">
              <label class="text-dark">Password:</label>
              <input type="password" class="form-control" id="validationDefault02" placeholder="Enter Your Password" required>
            </div>
        
            <div class="col-md-12 col-12 d-grid gap-2">
              <button class="btn btns border-0 btn-primary" style="background-color: #48A2B1;" type="submit"><b>Sign in</b></button>
            </div>
            <div class="col-12">
              <div class="form-check">
                <input class="form-check-input" type="checkbox" value="" id="invalidCheck2">
                <label class="form-check-label text-dark" for="invalidCheck2">
                  Remember Me?
                </label>
              </div>
              <button class="btn text-decoration-underline ps-4 " data-bs-target="#exampleModalToggle2"
               data-bs-toggle="modal" style="color: #0F90A6;">Register now</button> 
              </div>
      
              <div class="modal-footer text-center">
<div class="d-grid gap-2 col-lg-8 col-sm-12 mx-auto">
  <a class="btn btns text-light text-start " style="background-color: #3A5999;" href="#!" role="button"><i class="bi bi-facebook fs-5 p-3" ></i><b>Sign in with Facebook</b></a>
  <a class="btn btns text-light text-start " style="background-color: #04ABEF;" href="#!" role="button"><i class="bi bi-twitter fs-5 p-3"></i><b>Sign in with Twitter</b></a>
  <a class="btn btns text-light text-start " style="background-color: #F34234;" href="#!" role="button"><i class="bi bi-google fs-5 p-3 "></i><b>Sign in with Gmail</b></a>
              </div>
           </div>

          </form>




        </div>

      </div>
    </div>
  </div>
  <div class="modal fade" id="exampleModalToggle2" aria-hidden="true" aria-labelledby="exampleModalToggleLabel2" tabindex="-1">
    <div class="modal-dialog modal-dialog-centered">
      <div class="modal-content">
        <div class="modal-header">
          <h1 class="modal-title fs-5 text-dark " id="exampleModalToggleLabel2"><b>Sign up</b></h1>
          <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
        </div>
        <div class="modal-body">
          <form class="row g-3">
            <div class="col-md-12">
              <label class="text-dark">Email:</label>
              <input type="email" class="form-control" id="validationDefault03" placeholder="Enter Your Email" required>
            </div>
            <div class="col-md-12">
              <label class="text-dark">Username:</label>
              <input type="text" class="form-control" id="validationDefault04" placeholder="Enter Your Username" required>
            </div>
            <div class="col-md-12">
              <label class="text-dark">Password:</label>
              <input type="password" class="form-control" id="validationDefault05" placeholder="Enter Your Password" required>
            </div>
            <div class="col-md-12">
              <label class="text-dark">Confirm Password:</label>
              <input type="password" class="form-control" id="validationDefault06" placeholder="Enter Your Password" required>
            </div>
        
            <div class="col-md-12 col-12 d-grid gap-2">
              <button class="btn btns border-0 btn-primary" style="background-color: #48A2B1;" type="submit"><b>Sign up</b></button>
            </div>
      
  
          </form>
        </div>
        <div class="modal-footer">
          <button class="btn " data-bs-target="#exampleModalToggle" data-bs-toggle="modal">You Already Have an account?</button>
        </div>
      </div>
    </div>
  </div>
  <button class="btn btn-link text-dark  text-decoration-none" data-bs-toggle="modal" href="#exampleModalToggle" role="button">Sign in</button> 


<!-- Sign in as doctor -->

  <div class="modal fade" id="exampleModalToggle3" aria-hidden="true" aria-labelledby="exampleModalToggleLabel" tabindex="-1">
    <div class="modal-dialog modal-dialog-centered">
      <div class="modal-content">
        <div class="modal-header">
          <h1 class="modal-title fs-5 text-dark" id="exampleModalToggleLabel"><b>Sign in as doctor</b></h1>
          <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
        </div>
        <div class="modal-body">
          <form class="row g-3">
            <div class="col-md-12">
              <input type="text" class="form-control" id="validationDefault07" placeholder="Enter Your Username" required>
            </div>
            <div class="col-md-12">
              <input type="tel" class="form-control" id="validationDefault08" placeholder="Enter Your PhoneNumber" required>
            </div>
        
            <div class="col-md-12 col-12 d-grid gap-2">
              <button class="btn btns border-0 btn-primary" style="background-color: #48A2B1;" type="submit"><b>Sign in</b></button>
            </div>
            <div class="col-12">
              <div class="form-check">
                <input class="form-check-input" type="checkbox" value="" id="invalidCheck3">
                <label class="form-check-label text-dark" for="invalidCheck2">
                  Remember Me?
                </label>
                <button class="btn-link btn text-decoration-underline ps-4 d-none" data-bs-target="#exampleModalToggle6"
               data-bs-toggle="modal">Code Number</button> 
              </div>
              
            </div>
          </form>
        </div>

      </div>
    </div>
  </div>
  <div class="modal fade" id="exampleModalToggle6" aria-hidden="true" aria-labelledby="exampleModalToggleLabel2" tabindex="-1">
    <div class="modal-dialog modal-dialog-centered">
      <div class="modal-content">
        <div class="modal-header">
          <h1 class="modal-title fs-5" id="exampleModalToggleLabel2"><b>Code Number</b></h1>
          <p>Please enter the code number that has sent to your phone number </p>
          <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
        </div>
        <div class="modal-body">
          <form class="row g-3">
            <div class="col-md-12">
              
              <input type="email" class="form-control" id="validationDefault09" placeholder="Enter The code number" required>
            </div>
        
        
            <div class="col-md-12 col-12 d-grid gap-2">
              <button class="btn btns border-0 btn-primary" style="background-color: #48A2B1;" type="submit"><b>OK</b></button>
            </div>
      
  
          </form>
        </div>
        <div class="modal-footer">
          <button class="btn " data-bs-target="#exampleModalToggle3" data-bs-toggle="modal">Change Phone Number?</button>
        </div>
      </div>
    </div>
  </div>
       <button class="btn btn-secondary  border-0 text-light"  data-bs-toggle="modal" href="#exampleModalToggle3" role="button">Sign as doctor</button>

      </span>
    </div>
  </div>
</nav>
</div>


</template>





<script>
export default {

}
</script>
<style>

.home{
  color: #48A2B1;
}
.home:hover{
  color: #6bb5c2;
}
.nav-link.a{
  color:#3C3737;
}
.nav-link , .btn-link {
  display: inline-block;
  position: relative;
  color: #48A2B1;
}

.nav-link::after, .btn-link::after  {
  content: '';
  position: absolute;
  width: 100%;
  transform: scaleX(0);
  height: 2px;
  bottom: 0;
  left: 0;
  background-color: #48A2B1;
  transform-origin: bottom right;
  transition: transform 0.25s ease-out;
}

.nav-link:hover::after , .btn-link:hover::after {
  transform: scaleX(1);
  transform-origin: bottom left;
}

.btn-link:hover{
opacity: 0.6;
color: #48A2B1;

}

</style>
