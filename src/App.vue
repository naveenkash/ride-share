<template>
  <div id="app">
    <navbar />
    <app-header />
    <follow/>
    <estimate/>
    <howItWork/>
    <rideshare/>
    <news/>
    <HowMain/>
    <AppFooter/>
    <!-- <div class="h"></div> -->
  </div>
</template>

<script>
import navbar from "./components/navbar.vue";
import header from "./components/header.vue";
import follow from './components/flollow-path.vue'
import estimate from './components/fare-estimate'
import howItWork from './components/how-it-work';
import rideshare from './components/ride-sharing';
import news from './components/news'
import HowMain from './components/how-it-work-main'
import AppFooter from './components/footer'
export default {
  name: "app",
  components: {
    navbar,
    "app-header":header ,
    follow,
    estimate,
    howItWork,
    rideshare,
    news,
    HowMain,
    AppFooter
  }
};
</script>

<style>
.h {
  height: 200vh;
  width: 100%;
  background: green;
}
@import url("https://fonts.googleapis.com/css?family=Poppins&display=swap");
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Poppins", sans-serif;
  /* overflow-x: hidden; */
}
::selection {
  background: #313033;
  color: white;
}

.container {
  width: 1200px;
  margin: 0 auto;
  height: auto;
}
.clearfix {
  content: "";
  display: table;
  clear: both;
}
.f-h{
  width: 100%;
  height: auto;
}
.pad-m{
  padding: 80px 0;
}
.pad-xl{
  padding: 150px 0 80px 0;
}
.pad-t{
  padding-top: 80px;
}
@media screen and (max-width:1300px){
  .container{
    width: 1080px;
  }
}
@media screen and (max-width:1180px){
  .container{
    width: 950px;
  }
  
}
@media screen and (max-width:1050px){
  .container{
    width: 850px;
  }
  
}
@media screen and (max-width:900px){
  .container{
    width: 750px;
  }
  
}
@media screen and (max-width:800px){
  .container{
    width: 650px;
  }
  
}
@media screen and (max-width:700px){
  .container{
    width: 100%;
    padding: 0 20px;
  }
  
}
</style>
