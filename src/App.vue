<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<style lang="scss">
body{
  margin: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
.container{
  width: 90%;
  margin: auto;
}
a{
  text-decoration: none;
}
#nav {
  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #f261b4;;
    }
  }
}
.color-pink{
    color: #f261b4;
}
.logo{
  
      font-size: 1.6em;
    font-weight: 900;
}
.btn-pink{
  background: #f261b4;
  padding: 0.5rem 1rem;
  border-color: #f261b4;
  color:#f8f7f5;
  border:0px;
}
.btn-light{
  background: #f8f7f5;
  padding: 0.5rem 1rem;
  border-color: #f8f7f5;
  color:#f8f7f5
}
.w-50{
  width: 50%;
}
.btn-green{
    position: absolute;
    bottom: 0em;
    margin: 0 auto;
    display: block;
    width: 90%;
    border: none;
    color: #fff;
    background-color: #16c484;
    cursor: pointer;
    text-align: center;
    display: flex;
    align-items: center;
    justify-content: center;
    padding:0.3rem 0;
}
.grid{
  display: grid;
  grid-template-columns: auto auto auto auto;
  grid-column-gap: 50px;
  .grid-item {
    row-gap: 2rem;
  }
}
.flex{
  display: flex;
    flex-wrap: wrap;
    .mt-3{
      flex-grow: 1;
}
}
.mt-3{
  margin-top:3rem !important;
}
.mb-1{
  margin-bottom: 1rem;
}
.card{
  padding: 1.5rem;
  border: 1px solid #cccccc08;
  box-shadow: -1px 0px 13px 4px #f5f3f3;
  text-align: center;
}
.between{
  justify-content: space-between;
}
.evenly{
  justify-content: space-evenly;
}
.w-3{
  width: 33.333;
}
.mt-5{
  margin-top: 5rem;
}
.m-0{
  margin: 0;
}

@media (max-width: 990px){
.side-img {
    width: 80% !important;
    display: block;
    margin: auto;
}
.about__con {
    width: 80% !important;
    margin: 4em auto;
    text-align: center;
}
footer {
    flex-direction: column;
    text-align: center;
}
.text{
    text-align: center;
    margin: 10em 0 0 0;
    width: 100% !important;
}
.sm-none{
  display: none;
}
.category {
      width: 80% !important;
    margin: 0 auto;
}
.grid-card {
    // width: 80% !important;
    margin: 0 auto;
    height: auto;
}
.search-input{
    width: 82% !important;
}
}
</style>
