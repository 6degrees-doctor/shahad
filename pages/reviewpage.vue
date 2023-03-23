<template>
  <div>

    <div class="container-fluid ">
      <div class="row bg ps-4 py-3">

        <div class="col d-flex ">
          <NuxtLink to="/" class=" text-decoration-none text-light">Home></NuxtLink>
          <NuxtLink to="reviewpage" class=" text-decoration-none text-light">Review></NuxtLink>
          <a class=" text-decoration-none text-dark ps-1" disabled>Active Page</a>
        </div>
      </div>
    </div>

    <div class="container   shadow ">
      <div class="row rowcolor mt-5 rounded ">
        <div class="col-lg-4 col-md-12 col-12 ps-5 m-2">
          <img src="~/assets/images/doc2.jpg" class="img-fluid rounded-circle shadow imgd">
        </div>
        <div class="vr d-none d-sm-block" style="background-color: #48A2B1;"></div>
        <div class="col-lg-3 col-md-12 col-12 m-2 mt-5 ">
          <h5 class=""> <b>Dr. Mohammad Saleh</b> </h5>

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


          <div class="col-lg-12 col-12 col-sm-12">
            <h4><b>Pending Comments</b></h4> <!--This section only for authorized doctors  -->
            <div class="card">
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
            <div class="card" >
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


          <form @submit.prevent="writecomment" >
            <div v-if="err" class="
                        text-danger
                        mb-4
                      " role="alert">
              {{ err }}
            </div>
            <div v-if="success" class="
                      text-success
                        mb-4
                      " role="alert">
              Your comment has been send </div>

            <h4 class="mt-4"> <i class="bi bi-pencil-square "></i><b>Write a Review</b></h4>
            <hr>
              <div v-if="isAuthenticated" class=" col-lg-4 col-md-12 col-12  mb-3">
              <label for="text" class="form-label">Name: </label> 
              <input  v-model="name" type="text" class="form-control"  :placeholder="loggedInUser.username"  disabled>
            </div> 

            <div  v-if="!isAuthenticated" class=" col-lg-4 col-md-12 col-12  mb-3">
              <label for="text" class="form-label">Name: </label> 
              <input v-model="name" type="text" class="form-control"  placeholder="Enter Your Name.." >
            </div>

            
            <!-- <div class=" col-lg-4 col-md-12 col-12  mb-3">
               <label for="exampleFormControlInput1" class="form-label">Rate:</label>
            
              <div class="rating" >
                <i class=" rating__star bi bi-star-fill "></i>  
                <i class=" rating__star bi bi-star"></i>
                  <i class="rating__star bi bi-star"></i>
                  <i class="rating__star bi bi-star"></i>
                  <i class="rating__star bi bi-star"></i>
              </div>
            </div> -->


            <div class="col-lg-8 col-md-12 col-12 mb-3">
              <label for="text" class="form-label">Comment:</label>
              <input type="text" v-model="comments" class="form-control" id="exampleFormControlTextarea1" 
                placeholder="Write your comment..">
            </div>
            <div class=" d-flex justify-content-start">
              <div class="d-grid gap-2 col-lg-2 col-12">
                <button type="submit" class="btn btn-secondary  border-0 text-light">Send</button>
                <a href="" class="text-dark ps-3 mt-2 " data-bs-toggle="modal"
                  data-bs-target="#exampleModal">Anonymous?</a>
              </div>


              <!-- Button trigger modal -->
              <!-- Modal -->
              <!-- <div class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel"
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
              </div> -->
            </div>
          </form>
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
        <div class="card" > <!-- v-for="(user, key) in this.users" :key="key" -->
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
              <p class="fw-bold text-muted mb-0">nora</p>  <!--  {{ user.username }} -->
                  <p class="text-muted fw-light mb-4">
                   
                  </p> <!-- {{ user.comments.comment }} --> 
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
import { mapGetters } from 'vuex'
export default {

      data() {
        return {
          success: '',
          err: '',
         name: '',
          comments: '',
        
        
        }
      },
      methods: {
        async writecomment() {
          try {
            this.$axios.setToken(false)
            const requestBody = await this.$axios.post('/comments', {
              data:{
                 name: this.name,
              comments: this.comments ,
              },
            
            })
            this.success = true
          } catch (e) {
            if (e.response) this.err = e.response.data.error.message
          }
        },
      },

 computed: {
      ...mapGetters(['isAuthenticated' , 'loggedInUser']),
     },


  // methods: {
  //   async getInformation(endpoint, targetVar) {

  //     try {
  //       // fetch data from strapi
  //       const comment = await fetch(`${endpoint}`)
  //       const newData = await comment.json();
  //       targetVar = newData;

  //       if (targetVar == 'comment') {
  //         this.comment = newData;
  //       } else if (targetVar == 'users') {
  //         this.users = newData;
  //       }
  //       // console.log(`${targetVar[0].username}`);
  //     } catch (error) {
  //       console.log(error)
  //     }

  //   }
  // },
  // async mounted() {
  //   // Better way to call axois or any group of endpoints
  //   await this.getInformation('http://localhost:1337/api/comments', 'comments');
  //   await this.getInformation('http://localhost:1337/api/users?populate=*', 'users');
  //   console.log(this.users);
  //   console.log(this.comment);

  // },
  
   
 
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