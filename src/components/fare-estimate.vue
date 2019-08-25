<template>
  <div class="f-h pad-m fare">
    <div class="container">
      <div class="fare-wrapper clearfix">
        <div class="fare-content">
          <h1>Where to ?</h1>
          <p>How much does GoDrive cost in your city?</p>
          <p>Calculate a fare estimate for your next</p>
          <p>trip.Simply enter a pickup location and</p>
          <p>destination to get started..</p>
          <div class="fare-input-search">
            <input placeholder="Enter Pick Up Location" type="text" />
            <br />
            <input placeholder="Enter Dropp-Off Location" type="text" />
            <div class="green"></div>
            <div class="green-border"></div>
            <div class="red"></div>
            <div class="red-border"></div>
            <div class="border">

            </div>
          </div>
          <vehicle />
        </div>
      </div>
    </div>
    <div class="fare-img">
      <img id="fare-bkg" class="hide-fare" src="../assets/estimate.png" alt />
    </div>
  </div>
</template>
<script>
import vehicle from "./select-vehicle";
import '../animate.css'
export default {
  components: {
    vehicle
  },
  methods: {
    fareImgAnimation(pageOffset) {
      var fareContainer = document.querySelector(".fare");
      var fareImg = document.querySelector("#fare-bkg");
      var fareContainerOffsetTop = fareContainer.offsetTop;
      var fareClientHeight = fareContainer.clientHeight;
      var farehalfClientHeight = fareClientHeight / 2;
      var res = fareContainerOffsetTop - farehalfClientHeight;
      if (pageOffset >= res) {
        fareImg.classList.add("animated", "fadeInLeft","show-fare");
        
          fareImg.classList.remove('hide-fare');
      }
    }
  },
  created() {
    document.addEventListener("DOMContentLoaded", () => {
      window.addEventListener("scroll", () => {
        this.fareImgAnimation(window.pageYOffset);
      });
    });
  },
  destroyed() {
    window.removeEventListener("scroll", () => {
      this.fareImgAnimation(window.pageYOffset);
    });
  }
};
</script>
<style scoped>
.fare-wrapper {
  width: 100%;
  height: 100%;
}
.fare {
  position: relative;
  /* margin-top: 50px; */
  height:100vh;
  display: flex;
  width: 100%;
  align-items: center;
}
.show-fare{
  opacity:1;
}
.hide-fare{
  opacity: 0;
}
.fare-img {
 position: absolute;
    top: 50%;
    left: 0;
    /* max-width: 100%; */
    width: 55%;
    height: auto;
    transform: translate(-0%, -50%);
    /* margin-bottom: 140px;*/
}
.fare-img img {
  max-width: 100%;
  height: auto;
}
.fare-content {
  width: 40%;
  height: 100%;
  float: right;
  padding-left: 25px;
  /* padding-top: 200px; */
}
.fare-content h1 {
  margin-bottom: 30px;
}
.fare-content p {
  font-size: 14.5px;
  line-height: 30px;
}
.fare-input-search {
  width: 100%;
  height: auto;
  margin-top: 40px;
  padding: 0 45px;
  position: relative;
  /* -webkit-box-shadow: 0px 0px 10px 1px rgba(163,163,163,0.2);
-moz-box-shadow: 0px 0px 10px 1px rgba(163,163,163,0.2);
box-shadow: 0px 0px 10px 1px rgba(163,163,163,0.2); */
  -webkit-box-shadow: 0px 0px 34px 3px rgba(163, 163, 163, 0.2);
  -moz-box-shadow: 0px 0px 34px 3px rgba(163, 163, 163, 0.2);
  box-shadow: 0px 0px 34px 3px rgba(163, 163, 163, 0.2);
}
.green {
  width: 10px;
  height: 10px;
  border-radius: 50%;
  background: #27aa0a;
  position: absolute;
  top: 25px;
  left: 18px;
  /* animation: bubble 2s ease infinite; */
}
.green-border {
  position: absolute;
  top: 25px;
  left: 18px;
  width: 10px;
  height: 10px;
  border: 1px solid #27aa0a;
  border-radius: 50%;

  animation: bubble 2s ease infinite;
}
.border{
    width: 1px;
    height: 45px;
    border: 1px dashed rgba(106, 110, 117, 0.493);
    
  position: absolute;
    top: 34px;
    left: 22px;
}

@keyframes bubble {
  0% {
    transform: scale(1);
    opacity: 1;
  }
  10% {
    transform: scale(1.5);
    opacity: 0.8;
  }
  20% {
    transform: scale(1.8);
    opacity: 0.7;
  }
  30% {
    transform: scale(2);
    opacity: 0.6;
  }
  40% {
    transform: scale(2.3);
    opacity: 0.5;
  }
  50% {
    opacity: 0.4;
    transform: scale(2.5);
  }
  60% {
    opacity: 0.3;
    transform: scale(2.7);
  }
   70% {
    opacity: 0.2;
    transform: scale(2.7);
  }
  80% {
    opacity: 0.1;
    transform: scale(2.7);
  }
  100% {
    opacity: 0;
    transform: scale(2.7); 
  } 
}
.red {
  width: 10px;
  height: 10px;
  border-radius: 50%;
  background: #f32e01;
  position: absolute;
  bottom: 22px;
  left: 18px;
  /* animation: bubble2 1s ease infinite; */
}
.red-border{
    
  width: 10px;
  height: 10px;
  border-radius: 50%;
  border:1px solid #f32e01;
  position: absolute;
  bottom: 22px;
  left: 18px;
  animation: bubble 2s ease infinite;
}
.fare-input-search input {
  width: 100%;
  height: auto;
  padding: 18px 0px;
  font-size: 15px;
  border: none;
  outline: none;
}
.fare-input-search input:nth-child(1) {
  padding-bottom: 22px;
  border-bottom: 1px solid rgba(209, 209, 209, 0.459);
}

@media screen and (max-width:1180px){
  .fare-content{
    width: 45%;
  }
  
}
@media screen and (max-width:1050px){
  .fare-content{
    width: 50%;
  }
  .fare-img{
    width:50%;
  }
  
}
@media screen and (max-width:900px){
  .fare-content{
    width:55%;
  }
   .fare-img{
    width:45%;
  }
}
@media screen and (max-width:800px){
  
   .fare-img{
     display: none;
  }
  .fare-content{
    width: 100%;
    float: none;
  }
  .fare-content p{
    display: inline-block;
  }
  .fare-content p:last-of-type{
    margin-left: 5px;
  }
}
@media screen and (max-width:700px){
  .fare-content{
    padding: 0;
  }
}
</style>
