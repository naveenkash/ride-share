<template>
  <div class="f-h pad-m work-main">
    <div class="container">
      <div class="how-wrapper clearfix">
        <div class="how-it-work-con">
          <h1>How is it Work!</h1>
          <p>How much does GoDrive cost in your city? Calculate a fare estimate for your next trip. Simply enter a pickup location and destinationto get started. The new Driver app helps you earn smarter and supports you–like a partner–at every turn.</p>
          <a href="#">
            Explore
            <span>&rarr;</span>
          </a>
        </div>
      </div>
    </div>
    <!-- <div class="news-img">
            <img src="https://react-next-landing.redq.io/_next/static/images/how_it-c3a64dd28baf795641cfc060c74c46ae.svg" alt="">
    </div>-->
  </div>
</template>
<script>
export default {};
</script>
<style scoped>
.how-wrapper {
  width: 100%;
  height: auto;
}
.how-it-work-con {
  width: 40%;
  float: left;
  /* padding-top: 250px; */
}
.how-it-work-con h1 {
  margin-bottom: 30px;
  font-weight: bolder;
}
.how-it-work-con p {
  line-height: 32px;
  font-size: 14px;
  margin-bottom: 50px;
}
.how-it-work-con a {
  background: #8454ff;
  text-decoration: none;
  padding: 14px 26px;
  border-radius: 4px;
  color: white;
  font-size: 14px;
  transition: 0.3s;
  -webkit-transition: 0.3s;
  -moz-transition: 0.3s;
}

.how-it-work-con a span {
  margin-left: 10px;
}
.how-it-work-con a:hover {
  -webkit-box-shadow: 0px 5px 45px 1px rgba(132, 84, 255, 0.25);
  -moz-box-shadow: 0px 5px 45px 1px rgba(132, 84, 255, 0.25);
  box-shadow: 0px 5px 45px 1px rgba(132, 84, 255, 0.25);
}
.work-main {
  position: relative;
  background-image: url("https://react-next-landing.redq.io/_next/static/images/how_it-c3a64dd28baf795641cfc060c74c46ae.svg");
  display: flex;
  height: 100vh;
  background-size: 850px;
  -webkit-box-pack: center;
  justify-content: center;
  -webkit-box-align: center;
  align-items: center;
  padding: 120px 0px;
  overflow: hidden;
  background-repeat: no-repeat;
  background-position: 100% center;
}
.news-img {
  position: absolute;
  top: 0;
  right: 0;
  /* max-width: 100%; */
  width: 50%;
  height: auto;
  /* margin-bottom: 140px; */
}
.news-img img {
  max-width: 100%;
  height: auto;
}
@media screen and (max-width:1500px) {
  .work-main{
    background-size: 750px;
  }
}
@media screen and (max-width:1300px) {
  .work-main{
    background-size: 650px;
  }
}
@media screen and (max-width:1100px) {
  .work-main{
    background-size: 550px;
  }
}
@media screen and (max-width:900px) {
  .work-main{
    background-size: 450px;
  }
  
}
@media screen and (max-width:800px) {
  .work-main{
    background-size: 650px;
    background-image: none;
  }
  .how-it-work-con{
    width: 100%;
    float: none;
  }
}
</style>
