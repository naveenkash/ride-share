<template>
  <div class="header-container">
    <div class="container">
      <div class="header-content clearfix">
        <div class="header-wrapper">
          <div class="header">
            <div class="header-text">
              <h1>
                <strong>Get to where</strong>
              </h1>
              <h1>
                <strong>you want to be.</strong>
              </h1>
              <h1 id="light-text">It's in your hand.</h1>
            </div>
            <div class="header-email">
              <input placeholder="Enter Email Address" type="text" />
              <a href>Text Me A Link</a>
              <p>We’ll send you a text with a link to download the app.</p>
            </div>
            <div class="header-app"></div>
          </div>

          <div class="dwd-app">
            <div class="dwd-img">
              <img src="../assets/aps.png" alt />
            </div>
            <div class="dwd-img">
              <img src="../assets/pl.png" alt />
            </div>
          </div>
        </div>
        <div class="header-wrapper">
          <div class="header-img">
            <img id="man" src="../assets/man.png" alt />

            <img id="car" src="../assets/car.png" alt />
          </div>
        </div>
      </div>
    </div>
    <img id="Bkg" src="../assets/header-bkg.png" alt />
  </div>
</template>
<script>
export default {};
</script>
<style scoped>
.header-container {
  width: 100%;
  height: auto;
  overflow-x: hidden;
  position: relative;
  padding-bottom: 80px;
  /* background-image: url('../images/header-bkg.png'); */
}

.header-content {
  width: 100%;
  height: 100vh;
  padding: 100px 0;
}

.header-wrapper {
  width: 50%;
  height: 100%;
  float: left;
  position: relative;
}

.header {
  width: 100%;
  height: auto;
  margin-top: 12.5%;
  /* transform: translate() */
}

.header-text {
  width: 100%;
  height: auto;
}

.header-text h1 {
  font-size: 4.5em;
}

#light-text {
  font-weight: 400;
}

.header-email {
  width: 100%;
  margin: 30px 0;
  height: auto;
}

.header-email input {
  width: 350px;
  padding: 16px;
  font-size: 15px; 
  border: none;
  outline: none;
  -webkit-box-shadow: 0px 5px 45px 1px rgba(139, 141, 143, 0.25);
  -moz-box-shadow: 0px 5px 45px 1px rgba(139, 141, 143, 0.25);
  box-shadow: 0px 5px 45px 1px rgba(139, 141, 143, 0.25);
  margin-bottom: 30px;
  margin-right: 10px;
  border-radius: 4px;
}

.header-email a {
  padding: 14px 25px;
  text-decoration: none;
  background: rgb(132, 84, 255);
  color: white;
  font-size: 14px;
  border-radius: 4px;
  display: inline-block;
  transition: 0.3s;
}

.header-email a:hover {
  -webkit-box-shadow: 0px 5px 45px 1px rgba(132, 84, 255, 0.25);
  -moz-box-shadow: 0px 5px 45px 1px rgba(132, 84, 255, 0.25);
  box-shadow: 0px 5px 45px 1px rgba(132, 84, 255, 0.25);
}
.header-email p {
  font-size: 14.5px;
}

.header-img {
  width: 100%;
  height: 100%;
  position: relative;
}

#man {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 280px;
  height: auto;
  margin-left: 25px;
}

#car {
  position: absolute;
  bottom: 0;
  right: -75%;
  width: 600px;
  height: auto;
}
#Bkg {
  position: absolute;
  top: 0;
  right: -22px;
  width: 980px;
  height: auto;
  z-index: -1;
}
.dwd-app {
  width: 100%;
  height: auto;
  display: flex;
  align-items: center;
}
.dwd-app img {
  width: 160px;
  height: 50px;
  margin-right: 15px;
}
@media screen and (min-width: 2000px) {
  .header-wrapper{
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
  }
}
@media screen and (max-width:1800px){
  #car{
    right: -60%;
  }
}
/* @media screen and (max-width:1450px){
 #Bkg{
   width: 780px;
 }
} */
@media screen and (max-width:1400px){
  #car{
    right: -45%;
    height: 300px;
    width: 550px;
  }
  #man{
    height: 450px;
    width: 250px;
  }
   #Bkg{
   width: 780px;
 }
}
@media screen and (max-width:1300px) {
  .header-content{
    height: 100%;
  }
  .header-text h1{
    font-size: 4em;
  }
  #car{
    right: -35%;
    width: 440px;
    height: 250px;
  }
  #man{
        width: 200px;
    height: 350px;
  }
  .header-container{
    padding-bottom: 0;
  }
}
@media screen and (max-width:1180px) {
  .header-text h1 {
    font-size: 3.5em;
}
.header-email input{
  width: 300px;
}
#car{
  right: -45%;
}
#Bkg{
  width: 700px;
}
}
@media screen and (max-width:1050px) {
  .header-text h1{
    font-size: 3em;
  }
    #car{
    right: -45%;
    width: 400px;
    height: 200px;
  }
  #man{
        width: 180px;
    height: 300px;
  }
  .header-email input{
    width: 250px;
  }
  .header-email a{
    padding: 14px 20px;
  }
}
@media screen and (max-width:990px) {
  #Bkg,#car,#man{
    display: none;
  }
  .header-wrapper{
    width: 100%;
    float: none;
  }
  .header-container{
    
    background: #FAF8FF;
  }
  .header-email input{
    width: 50%;
  }
   .header-wrapper:nth-child(2){
    display: none;
  }
  .header{
    margin-top: 12%;
  }
  .header-text h1 {
    font-size: 3.5em;
    display: inline-block;
}
}
@media screen and (max-width:900px) {
  .header-text h1{
    font-size: 3.3em;
  }
}
@media screen and (max-width:440px) {
  .header-text h1{
    font-size: 2.5em;
  }
  .header-email a{
    padding: 15px 16px;
    font-size: 12px;

}
}


</style>
