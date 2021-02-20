<template>
  <div id="app">
    <div class="container">
      <div id="nav">
       <div class="flex between">
          <h2 class="color-pink logo m-0">huntr</h2>
          <svg class="md-none" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1" id="Capa_1" x="0px" y="0px" viewBox="0 0 384.97 384.97" style="enable-background:new 0 0 384.97 384.97;" xml:space="preserve" width="512px" height="512px"><g><g>
            <g id="Menu_1_">
              <path d="M12.03,120.303h360.909c6.641,0,12.03-5.39,12.03-12.03c0-6.641-5.39-12.03-12.03-12.03H12.03    c-6.641,0-12.03,5.39-12.03,12.03C0,114.913,5.39,120.303,12.03,120.303z" data-original="#000000" class="active-path" data-old_color="#000000" fill="#FFFFFF"/>
              <path d="M372.939,180.455H12.03c-6.641,0-12.03,5.39-12.03,12.03s5.39,12.03,12.03,12.03h360.909c6.641,0,12.03-5.39,12.03-12.03    S379.58,180.455,372.939,180.455z" data-original="#000000" class="active-path" data-old_color="#000000" fill="#FFFFFF"/>
              <path d="M372.939,264.667H132.333c-6.641,0-12.03,5.39-12.03,12.03c0,6.641,5.39,12.03,12.03,12.03h240.606    c6.641,0,12.03-5.39,12.03-12.03C384.97,270.056,379.58,264.667,372.939,264.667z" data-original="#000000" class="active-path" data-old_color="#000000" fill="#FFFFFF"/>
              </g><g></g><g></g><g></g><g></g><g></g><g></g></g></g> 
            </svg>
       </div>
        <div class="w-70 mobile-nav flex between">
            <ul class="flex">
                <li> <router-link to="/">Get Jobs</router-link> </li>
                <li><router-link to="/about">Post Jobs</router-link></li>
            </ul>
            <ul class="flex">
                <li><router-link to="/login" class="btn-light color-pink">Login</router-link></li>
                <li><router-link to="/about" class="btn-pink color-light">Signup</router-link></li>
            </ul>
            <h2 class="md-none">X</h2>
        </div>
    </div>
    </div>
  </div>
</template>

<style lang="scss">
#nav {
  display: flex;
  justify-content: space-between;
  padding: 2rem 0;
  ul{
    list-style-type: none;
    display: flex;
    list-style:none;
    li {
      padding: 0 2rem;
    }
  }
}
 .color-light{
    color:#f8f7f5 !important;
  }
  .color-pink{
    color: #f261b4 !important  ;
  }
@media (min-width: 990px){
  .md-none{
      display: none;
    }
    .w-70{
      width: 70%;
    }
}
@media (max-width: 990px){
  #nav {
  display: block;
  padding: 2rem 0;
  ul{
      display: block;
      line-height: 3;
      li {
        padding: 0 2rem;
      }
    }
  }
  .flex{
    display: block;
  }
  #nav svg{
    position: absolute;
    right: 0px;
    top: 33px;
    width: 11rem;
    height: 43px;
    text-align: right;
  }
  .mobile-nav{
    background: white;
    position: absolute;
    min-width: 100%;
    max-width: 100%;
    left: 0;
    top: 0;
    min-height: 100%;
    z-index:9;
    display: none;
    .flex{
      display: block;
    }
    h2{
      position: absolute;
      right: 2rem;
      top: 0;
    }
  }
}
</style>
