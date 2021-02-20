<template>
  <div>
    <div class="container">
      <h2 class="latest-news">Latest Jobs </h2>
      <div class="grid-latest">
        <div class="grid-card mt-3" v-for="(job, index) in jobs" :key="index">
          <h4 class="card-title mb-2">{{job.title}}</h4>
          <div class="details">
            <p class="m-0 remote">{{job.location}} </p>
            <p class="m-0 color-pink py-1">{{job.published_at.for_humans}}</p>
          </div>
          <div class="mt-3">
            <img :src="job.company.avatar" alt="company logo" class="responsiv-img">
            <h5 class="m-0">{{job.company.name}}</h5>
          </div>
          <div class="position-relative">
            <vue-link class="btn-green" :to="job.url">Appy Now</vue-link>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  data () {
    return {
      jobs: []
    }
  },
  created() {
    axios.get('https://vuejobs.com/api/jobs')
      .then(response => (this.jobs = response.data))
      .catch(error => console.log(error))
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style  lang="scss">
.responsiv-img {
    width: 2em;
}
.py-1{
  padding:1rem 0;
}
.mt-3{
  margin-top: 3rem;
}
.grid-latest{
  max-width: 1200px;
    margin: 2em auto;
    grid-row-gap: 40px;
    grid-column-gap: 40px;
    -moz-column-gap: 40px;
    column-gap: 100px;
    display: grid;
    grid-template-columns: repeat(auto-fill,minmax(200px,1fr));
    grid-auto-rows: 60px
}
.grid-card{
      position: relative;
    padding: 1em;
    width: 100%;
    height: 20rem;
    grid-row-end: span 4;
    background-color: #fff;
    box-shadow: 0 0 106px -59px #adabad;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
a {
  color: #42b983;
}
.relative{
  position: relative;
}
.latest-news{
    font-size: 2.4em;
    margin: 0;
    font-weight: 900;
}
.m-0{
  margin:0;
}
.card{
  padding: 1.5rem;
  border: 1px solid #cccccc08;
  box-shadow: -1px 0px 13px 4px #f5f3f3;
  .card-title{
    font-size:1rem;
    margin-bottom:3rem;
    margin-top: 0;
    font-weight: 700;
    line-height: 1.8;
  }
  .remote{
    color:#f261b4;
    font-size:1rem;
    font-weight: bold;
  }
  .details{
    margin-bottom: 3rem;
  }
  p{
    font-size:1rem;
    font-weight: bold;
  }
}

.mt-3{
  margin-top:3rem;
}
.mb-2{
  margin-bottom: 4rem;
}
</style>
