<template>
  <div class="home">
      <div class="flex">
        <div class="w-50 login-img">
            <img src="../../public/img/login-bg.jpg" />
        </div>
        <div  class="w-50 form-div flex">
          <div class="form-content">
              <div class="login__header">
                <a href="/" class="logo">huntr</a>
                <h3 class="login__heading">Need a job? 
                  <template v-if="isSignup">Login</template>
                  <template v-else>Signup</template>
                </h3>
              </div>
              <form action="login" class="login__form text-center" @submit.prevent="handleSubmit" v-if="!isSignup">
                <input type="text" placeholder="Your name" autocomplete="name" class="" v-model="first_name">
                <input type="email" placeholder="Email Address" autocomplete="email" class="" v-model="email">
                <input type="password" placeholder="Password" required="required" class="" v-model="password">
                <input type="submit" value="Register" required="required" class="bg-black cursor-pointer text-center">
              </form>
              <form action="login" class="login__form text-center" v-if="isSignup">
                <input type="email" placeholder="Email Address" autocomplete="email" class="">
                <input type="password" placeholder="Password" required="required" class="">
                <input type="submit" value="Login" required="required" class="bg-black cursor-pointer text-center">
              </form>
              <div>Don't have an account? 
                <a href="#" class="" v-if="isSignup" @click="isSignup =!isSignup"> Sign Up</a> 
                <a href="#" class=""  v-if="!isSignup" @click="isSignup =!isSignup">Login</a>
                
              </div>
          </div>
        </div>
      </div>
  </div>
</template>

<script>

export default {
  name: 'login',
  data(){
    return{
      isSignup: true,
      first_name: '',
      email: '',
      password: ''
    }
  },
  methods :{
    handleSubmit(){
      const data = {
        first_name: this.first_name,
        email: this.email,
        password: this.password
      }
      if(!this.first_name || !this.email || !this.password){
          console.log('input all field')
      }else{
      console.log(data)
    }
    }
  }
}
</script>

<style lang="scss" scoped>
  body{
      box-sizing: border-box; 
      margin: 0;
      padding: 0;
  }
  .cursor-pointer{
    cursor:pointer;
  }
  .text-center{
    text-align: center;
  }
  .w-50{
    width: 50%;
    img{
      width: 100%;
      height: 100vh;
      -o-object-fit: cover;
      object-fit: cover;;
    }
  }
  .login-img{
    position: relative;
  }
  .login-img::after{
      position: absolute;
      height: 100%;
      width: 100%;
      background-image: linear-gradient(rgba(0,0,0,.2),rgba(0,0,0,.4),rgba(0,0,0,.6),rgba(0,0,0,.94));
      top: 0;
      left: 0;
      content: '';
  }
  .login__form{
    display: grid;
    margin-top: 3rem;
    input{
      margin-bottom: 2rem;
    }
  }
  .form-div{
    justify-content: center;
    align-items: center;
    h3{
      margin-top: 1rem;
    }
    .logo{
      color: #f261b4;
    }
  }
  .form-content{
    width: 58%;
    text-align: center;
    input{
      line-height: 4;
    padding: 0 1rem;
    border-radius: 6px;
    border: 0;
    background: #f4f4f5;
    }
  }
  input:focus{
    outline: none;
    border:none;
  }
  .bg-black{
    background-color: rgb(7, 6, 6) !important;
    color:#f8f7f5;
  }
</style>