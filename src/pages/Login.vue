<template>
  <div class="page-header">
    <div
      class="page-header-image"
      style="background-image: url('img/login.jpg')"></div>
    <div class="content">
      <div class="container">
        <div class="col-md-5 ml-auto mr-auto">
          <card type="login" style="max-width: 420px;">
            <div slot="header" class="logo-container mr-auto ml-auto m-3">
              <img v-lazy="'img/tu-logo.png'" alt="" />
            </div>
            <div class="card-title font-weight-bold text-uppercase">Sign in to access your account!</div>
              
              <div class="card-body">
                <label class="pull-left">Email Address</label>
                <input
                  v-modal="email"
                  type="email"
                  class="input form-control p-3"
                  placeholder="Enter your Email Address"
                />

                <label class="pull-left">Password</label>
                  <input
                    type="password"
                    class="input form-control p-3"
                    placeholder="Enter your Password"
                  />

                  <div class="card-footer text-center">
                    <a
                      class="btn btn-primary btn-round btn-lg"
                      @click="loggedIn"
                      >Login</a>
                  </div>
              </div>

                <hr>
                <!-- <div>
                    <a class="link footer-link">
                      <i class="fab fa-instagram"></i>
                      <i class="fab fa-facebook"></i>
                      <i class="fab fa-mail"></i>
                    </a>
                </div> -->
            </card>
          </div>
        </div>
      </div>
    <main-footer></main-footer>
  </div>
</template>
<script>
import { Card, Button, FormGroupInput } from "@/components";
import MainFooter from "@/layout/MainFooter";
export default {
  name: "login-page",
  bodyClass: "login-page",
  components: {
    Card,
    MainFooter,
    [Button.name]: Button,
    [FormGroupInput.name]: FormGroupInput,
  },
  data(){
    return{
      users: [],
      userForm: {
        email: "",
        password: ""
      }
    }
  },
  methods: {
    loggedIn(){
      console.log('logged in successful')
    }
  }
};
</script>
<style>
.card-title{
  color: black;
}
.card-body{
  padding: 0;
}
label{
  padding: 5px;
  color: black;
}
</style>
