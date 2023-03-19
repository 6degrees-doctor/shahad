<template>
<div> 
    <div class="container-fluid ">
        <div class="row bg ps-4 py-3">
  
          <div class="col d-flex ">
            <NuxtLink to="/" class=" text-decoration-none text-light">Home></NuxtLink>
            <NuxtLink to="login" class=" text-decoration-none text-light">Sign in</NuxtLink>
            <a class=" text-decoration-none text-dark ps-1" disabled>Active Page</a>
          </div>
        </div>
      </div> 


<div class="container shadow mt-5 w-50">
    <div class="row rowcolor rounded mt-5 d-flex justify-content-center ">
<form @submit.prevent="userLogin" >

   <h1 class="text-dark">Sign in </h1>
    <div id="emailHelp" class="form-text">
    <div v-if="err"
    class=" p-4 mb-4 text-sm text-red-700 bg-red-100 rounded-lg dark:bg-red-200 dark:text-red-800 " role="alert" >
    {{ err }}
  </div>   
</div>

 <div class="col-lg-8 col-md-12 col-12 ">


    <div class="mb-3">
    <label for="email" class="form-label" >Email</label>
    <input v-model="email" placeholder="Enter your email" class="form-control" type="email" required > 
</div>

<div class="mb-3">
    <label for="password" >password</label>
    <input v-model="password" type="password" placeholder="Enter your password" class="form-control" required > 
    </div>

      <div class=" mb-3 form-check">
        <input type="checkbox" class="form-check-input" id="exampleCheck1">
        <label class="form-check-label" for="exampleCheck1">Remember me</label>
      </div> 
    
          <button class="btn btn-secondary border-0" type="submit" >Sign in </button>
<NuxtLink to="register">Don't have an account yet?</NuxtLink>
          <div class=" d-flex align-items-center my-4">
            <hr>
            <p class="text-center fw-bold mx-3 mb-0 text-muted">OR</p>
          </div>

          <a class="btn btn-primary btn-lg btn-block" style="background-color: #3b5998" href="#!"
            role="button">
            <i class="bi bi-facebook"></i>Continue with Facebook
          </a>
          <a class="btn btn-primary btn-lg btn-block" style="background-color: #55acee" href="#!"
            role="button">
            <i class="bi bi-twitter"></i>Continue with Twitter</a>
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