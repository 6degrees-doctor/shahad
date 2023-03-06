<template>
<div>
  <div class="container">
    <div class="row bg ps-4 py-3">

        <div class="col d-flex ">
        <NuxtLink to="/" class=" text-decoration-none text-light">Home></NuxtLink>
        <NuxtLink to="contact" class=" text-decoration-none text-light">Contact></NuxtLink>
        <a class=" text-decoration-none text-dark ps-1" disabled >Active Page</a>
        </div>
        </div>
      </div>

<div class="container shadow">
<div class="row rowcolor mt-5 ps-5 py-5">
    <div class="col-lg-4 col-12">
<img src="~/assets/images/news.png" alt="" class="img-fluid mt-5">
    </div>
   
<div class="col-lg-8 col-12 mt-5 gap-2 d-grid">
<h1>Get Touch With Us!</h1>

<label for="exampleFormControlInput1" class="form-label">Name:</label>
<input type="text" class="form-control" id="contactname" placeholder="Enter Your Name">


<label for="exampleFormControlInput1" class="form-label">Email:</label>
<input type="email" class="form-control" id="contactemail" placeholder="name@example.com">

<label for="exampleFormControlTextarea1" class="form-label">Message:</label>
  <textarea class="form-control" id="conatctmessage" rows="3"></textarea>
<div class="gap-2 d-grid col-12 col-lg-4 mt-4"> 
  <button class="btn btn-secondary">Send</button>
</div>
</div>

</div>
</div>




</div>

</template>

<style>
</style>