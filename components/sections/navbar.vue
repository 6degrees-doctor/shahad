<template>
  <div>

    <nav class="navbar navbar-expand-lg bg-body-tertiary shadow">
      <div class="container-fluid  ">
        <img src="~/assets/images/logo.png" class="img-fluid" style="width: 8rem;">
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent"
          aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class=" collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav me-auto mb-2 mb-lg-0 ">
            <li class="nav-item  ">

              <NuxtLink to="/" class="nav-link home ms-4 "><b>Home</b>
              </NuxtLink>
            </li>
            <li class="nav-item">
              <NuxtLink to="reviewpage" class="nav-link a ms-4">Review
              </NuxtLink>
            </li>
          
          </ul>
          <span class="navbar-text">


<a  v-if="isAuthenticated" > 

   Welcome back! <b>{{ loggedInUser.username }}</b></a>
  <a
  v-if="isAuthenticated"
  class="text-danger p-2  "
  href="/logout"
  @click.prevent="userLogout"
  >Logout</a>

            <NuxtLink
            v-if="!isAuthenticated"
            class="btn btn-secondary  border-0 text-light"
            to="login"
            >Sign In</NuxtLink>


          </span>
        </div>
      </div>
    </nav>
  </div>
</template>


<script>

import { mapGetters } from 'vuex'
    export default {
      computed: {
        ...mapGetters(['isAuthenticated' , 'loggedInUser']),
      },
      methods: {
        async userLogout() {
          await this.$auth.logout()
        },
      },
    }
</script>


<style>
.home {
  color: #48A2B1;
}

.home:hover {
  color: #6bb5c2;
}

.nav-link.a {
  color: #3C3737;
}

.nav-link {
  display: inline-block;
  position: relative;
  color: #48A2B1;
}

.nav-link::after{
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

.nav-link:hover::after{
  transform: scaleX(1);
  transform-origin: bottom left;
}
.iconuser{
  font-size: large;
}

</style>
