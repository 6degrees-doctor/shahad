<template>
<div>
    <div class="container-fluid ">
        <div class="row bg ps-4 py-3">
  
          <div class="col d-flex ">
            <NuxtLink to="/" class=" text-decoration-none text-light">Home></NuxtLink>
            <NuxtLink to="register" class=" text-decoration-none text-light">Sign up</NuxtLink>
            <a class=" text-decoration-none text-dark ps-1" disabled>Active Page</a>
          </div>
        </div>
      </div> 

      <div class="container shadow mt-5 ">
        <div class="row rowcolor rounded   "> 
        <h1 class="text-dark text-center">Sign up</h1>
        <hr>
            <form @submit.prevent="userRegister" class=" d-flex justify-content-center">
              <div class="col-lg-8 col-md-12 col-12 ">
                <div
            v-if="err"
            class="
              text-danger
              mb-4
              text-sm text-red-700
              bg-red-100
              rounded-lg
              dark:bg-red-200 dark:text-red-800
            "
            role="alert"
          >
            {{ err }}
          </div>
          <div
            v-if="success"
            class="
            text-success
              mb-4
            "
            role="alert"
          >
            Your account has been created successfully you can now
            <NuxtLink class="font-medium text-dark" to="login">Login</NuxtLink>
          </div>
                <div class="col">
                    <div class="mb-3">
                        <label for="username" class="form-label">Username</label>
                        <input type="text" v-model="username" class="form-control" id="exampleInputEmail1" placeholder="Enter Your Username">
                      </div>
               
                    <div class="mb-3">
                  <label for="email" class="form-label">Email address</label>
                  <input v-model="email" type="email" class="form-control" id="exampleInputEmail1" placeholder="Enter Your Email">
                 
                </div>
                <div class="mb-3">
                  <label for="password" class="form-label">Password</label>
                  <input v-model="password" type="password" class="form-control" id="exampleInputPassword1" placeholder="Enter Your Password">
                </div>
                <div class="col gap-2 d-grid text-center my-5 ">
                <button type="submit" class="btn btn-secondary border-0 ">Register</button>
                </div>
        </div></div>
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
          success: false,
          err: null,
          username: '',
          email: '',
          password: '',
        }
      },
      methods: {
        async userRegister() {
          try {
            this.$axios.setToken(false)
            await this.$axios.post('auth/local/register', {
              username: this.username,
              email: this.email,
              password: this.password,
            })
            this.success = true
          } catch (e) {
            if (e.response) this.err = e.response.data.error.message
          }
        },
      },
    }
</script>

<style>
</style>