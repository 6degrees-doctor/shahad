<template>
  <div class="bg">
  <div class="container">
    <div class="row p-5 ps-5 mt-5 text-light">



      <div class="col text-light">
<img src="image/logo2.png" class="img-fluid" style="width: 8rem">
<p class="text-light"> Lorem ipsum dolor sit amet,<br> consectetur adipiscing elit, </p>
      </div>

      <div class="col  ">
        <h5><b>Pages</b> </h5> 
<NuxtLink to="/" class="text-decoration-none"><a class="text-light text-decoration-none a" href="#"> Homepage</a></NuxtLink><br>
<NuxtLink to="aboutus" class="text-decoration-none"><a class="text-light text-decoration-none a"  href="#"> About us</a></NuxtLink><br>
<NuxtLink to="reviewpage" class="text-decoration-none"><a class="text-light text-decoration-none a"  href="#"> Review</a></NuxtLink><br>
<NuxtLink to="contact" class="text-decoration-none"><a class="text-light text-decoration-none a"  href="#"> Contact</a></NuxtLink><br>
       
      </div>

      <div class="col  ">
        <h5><b> Links</b></h5> 
<a class="text-light text-decoration-none a"  href="#"> Sign in as doctor</a><br>
<a class="text-light text-decoration-none a"  href="#"> Register</a>

      </div>

      <div class="col  ">
        <h5><b> Follow us</b></h5> 
        <div class="d-flex gap-3 social fs-5">
      <a href="http://www.twitter.com" class="text-light a"> <i class="bi bi-twitter " ></i></a> 
      <a href="http://www.facebook.com" class="text-light a"> <i class="bi bi-facebook"></i></a> 
        <a href="http://www.instagram.com" class="text-light a"> <i class="bi bi-instagram"></i></a> 
</div>
      </div>
        </div>
     </div>
    </div>

    
</template>

<style>
.bg{
  background-color: #48A2B1;

}
.a:hover{
opacity: 0.7;
}

/*.rect{
fill: rgba(152, 208, 218, 0.44);
transform: rotate(-15.95deg);
*/


</style>