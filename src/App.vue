<template>
  <div>
    <hove-v/>
    <nav-bar/>
    <about-me/>
    <my-portfolio/>
    <div data-aos="zoom-in-down">
      <work-v/>
    </div>
    
  </div>
</template>

<script>
import AboutMe from './components/about_me/AboutMe.vue'
import HoveV from './components/home/HoveV.vue'
import MyPortfolio from './components/my_works/MyPortfolio.vue'
import NavBar from './components/navbar/NavBar.vue'
import WorkV from './components/work/WorkV.vue'
  export default {
    components: { NavBar, HoveV, AboutMe, MyPortfolio, WorkV },

  }
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Oswald:wght@300;400;500;600;700&display=swap');
@import url('https://fonts.googleapis.com/css2?family=IBM+Plex+Sans+Thai:wght@100;200;300;400;500;600;700&display=swap');

html {
  scroll-behavior: smooth;
}
body {
  font-family: "IBM Plex Sans Thai", sans-serif;
  margin: 0;
  padding: 0;
}

li {
  list-style: none;
}

ul {
  padding: 0;
}
a {
  text-decoration: none;
}

.container {
  max-width: 1170px;   
  margin: 0 auto;
  padding: 50px;
}

h1 {
  margin: 0;
}

p {
  margin: 0;
}

.h1 {
  text-align: center;
} 

</style>