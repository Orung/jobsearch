<template>
  <div class="home">
     <img alt="background image" class="bg-img" src="../../public/img/home-bg.png">
    <NavBar />
    <div>
      <img alt="background image" class="curve-icon" src="../../public/img/curve.png">
    </div>
    <div class="container"> 
      <div class="text mt-5">
        <h5>GET STARTED</h5>
        <h2>Find Your Dream Job</h2>
        <p>We will boost your skills and profile, provide you with personalised career guidance and match you with the right opportunities,
          so that you can be the Best and the Brightest.</p>
      </div>
    </div>
    <div class="container">
      <div class="mt-10">
        <input class="search-input" type="text" placeholder="Job Title or Keyword">
        <button type="submit" class="btn btn-pink">Submit</button>
      </div>
    </div>
  <div class="">
    <LatestNews />
  </div>
  <div class="container mt-5">
    <h2 class="latest-news mt-3">Job Category</h2>
    <div class="job-category">
        <div class="card category mt-3">
          <div class="details">
          <h5 class="category-title mb-2">Design</h5>
            <p class="m-0 remote">150 Job Vacancy </p>
          </div>
        </div>
        <div class="card category mt-3">
          <div class="details">
          <h5 class="category-title mb-2">Design</h5>
            <p class="m-0 remote">150 Job Vacancy </p>
          </div>
        </div>
        <div class="card category mt-3">
          <div class="details">
          <h5 class="category-title mb-2">Design</h5>
            <p class="m-0 remote">150 Job Vacancy </p>
          </div>
        </div>
      </div>
  </div>
  <div class="container mt-3">
    <div class="flex evenly mt-5">
      <div class="side-img">
        <img src="../../public/img/bg-card.png">
      </div>
      <div class="about__con">
        <h2>We will help you get your dream job easy</h2>
        <p>We connect tech talents with the right job and have helped a lot of people (and counting) gain access to tech jobs across the World. 
          We Assess We help techies assess their skill-level or talent based on their ability to solve problems, learning speed, and strength of character.</p>
      </div>
    </div>
  </div>
  <Footer />
  </div>
</template>

<script>
// @ is an alias to /src
import NavBar from '@/components/NavBar.vue'
import LatestNews from '@/components/LatestNews.vue'
import Footer from '@/components/Footer.vue'
export default {
  name: 'Home',
  components: {
    NavBar,
    LatestNews,
    Footer
  }
}
</script>
<style lang="scss" scoped>
.mt-5{
  margin-top: 5rem;
}
.home{
  .bg-img{
    position: absolute;
    right: 0;
    z-index: -1;
    top: -2em;
    width: 50%;
  }
 .curve-icon{
    width: 8em;
    position: absolute;
    left: 0;
    top: 6rem;
  }
}
.mt-5{
  margin-top: 10rem;
}
.text{
      width: 40%;
  h5{
    margin-top: 4rem;
        color: #f261b4;
    text-transform: uppercase;
    margin-bottom: 0;
  }
  h2{
    font-size: 2.8em;
    margin: 0;
    font-weight: 900;
  }
}

.search-input{
    padding: 7px;
    border-radius: 0;
    border-color: aliceblue;
    border: 1px solid #eaecef;
    width: 31%;
    height: 25px;
    }
  .btn{
      height: 2.5rem;
    }
    .mt-10{
          margin: 10em 0;
    }
.latest-news{
    font-size: 2.4em;
    margin: 0;
    font-weight: 900;
}
.side-img{
  position: relative;
  width: 35%;
  img{
    width: 100%;
  }
}
.about__con {
    width: 40%;
    h2{
      font-size: 2.5em;
      color: #212121;
    }
  p{
    color: #707070;
    margin-top: 2em;
    line-height: 1.6em;
  }
}
.side-img::after{
    z-index: -1;
    content: "";
    right: 1em;
    bottom: 1em;
    width: 100%;
    height: 100%;
    border: .1em solid #f261b4;
    position: absolute;
}
.job-category{
  max-width: 1000px;
    margin: 2em auto;
    grid-row-gap: 40px;
    grid-column-gap: 40px;
    -moz-column-gap: 40px;
    column-gap: 200px;
    display: grid;
    grid-template-columns: repeat(auto-fill,minmax(200px,1fr));
    grid-auto-rows: 40px;
}
.category{
      color: #707070;
    text-align: center;
    position: relative;
    padding: 1em;
    width: 100%;
    height: 13em;
    grid-row-end: span 4;
    background-color: #fff;
    display: flex;
    align-items: center;
    justify-content: center;
}
</style>