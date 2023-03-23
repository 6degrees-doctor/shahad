<template>
<div> 
    <div class="container-fluid ">
        <div class="row bg ps-4 py-3">
  
          <div class="col d-flex ">
            <NuxtLink to="/" class=" text-decoration-none text-light">Home></NuxtLink>
            <NuxtLink to="login" class=" text-decoration-none text-light">Sign in></NuxtLink>
            <a class=" text-decoration-none text-dark ps-1" disabled>Active Page</a>
          </div>
        </div>
      </div> 


<div class="container-fluid shadow mt-5 " >
    <div class="row rowcolor rounded mt-5  ">
  <h1 class="text-dark text-center">Sign in </h1>
  <hr>
<form @submit.prevent="userLogin" class=" d-flex justify-content-center">

   

 <div class="col-lg-8 col-md-12 col-12 ">
 <div v-if="err"
    class="  mb-4 text-sm text-danger  " role="alert" >
    {{ err }}
 
</div>

    <div class="mb-3">
    <label for="email" class="form-label" >Email:</label>
    <input v-model="email" placeholder="Enter your email" class="form-control" type="email" required > 
</div>

<div class="mb-3">
    <label for="password" >password:</label>
    <input v-model="password" type="password" placeholder="Enter your password" class="form-control" required > 
    </div>

      <div class=" mb-3 form-check">
        <input type="checkbox" class="form-check-input" id="exampleCheck1">
        <label class="form-check-label" for="exampleCheck1">Remember me</label>
      </div> 
    
       <div class="col gap-2 d-grid text-center">
          <button class="btn btn-secondary border-0 " type="submit" >Sign in </button>
       
<NuxtLink to="register" class="text-dark ">Don't have an account yet?</NuxtLink>
          </div>

<div class=" my-4 text-center "> 
         <p class="fw-bold mx-3 mb-0 text-muted">OR </p>  
          </div>

          <div class="col gap-2 d-grid  ">
            <a class="btn btn-primary btn-lg btn-block border-0" style="background-color: #CA332A" href="#!"
            role="button">
            <i class="bi bi-google socialmedia "></i>Continue with Gmail
          </a>
          <a class="btn btn-primary btn-lg btn-block border-0" style="background-color: #3b5998" href="#!"
            role="button">
            <i class="bi bi-facebook socialmedia"></i>Continue with Facebook
          </a>
          <a class="btn btn-primary btn-lg btn-block border-0" style="background-color: #55acee" href="#!"
            role="button">
            <i class="bi bi-twitter socialmedia"></i>Continue with Twitter</a>
          </div>
          </div>
    </form>
</div>
</div>
    </div>

</template>

<script>

export default {
      auth: 'guest',
      data() {
        return {
          err: null,
          email: '',
          password: '',
        }
      },
      methods: {
        async userLogin() {
          try {
            await this.$auth.loginWith('local', {
              data: { identifier: this.email, password: this.password },
            })
          } catch (e) {
            if (e.response) this.err = e.response.data.error.message
          }
        },
      },
    }
</script>
