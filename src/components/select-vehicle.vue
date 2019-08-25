<template>
  <div class="f-h">
    <div class="vehicle-wrapper">
      <div class="vehi-con">
        <div class="select-vehicle">
          <div @click="bikeClick" :class="{'bike-bkg':this.bikeClicked}" class="vh-bike">
            <img src="../assets/mini-b.png" alt />
          </div>
          <div @click="carClick" :class="{'bike-bkg':this.carClicked}" class="vh-car">
            <img src="../assets/mini-c.png" alt />
          </div>
        </div>
        <div class="get-est">
          <a href>Get Estimate</a>
        </div>
      </div> 
     
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      bikeClicked: true,
      carClicked: false
    };
  },
  methods: {
    bikeClick() {
      this.bikeClicked = true;
      this.carClicked = false;
    },
    carClick() {
      this.bikeClicked = false;
      this.carClicked = true;
    }
  }
};
</script>
<style scoped>
.vehicle-wrapper {
  width: 100%;
  height: 100%;
  margin-top: 50px;
}
.vehi-con{
      width: 100%;
 height: auto;
 display: flex;
 align-items: center;
}
.select-vehicle {
 width: 100%;
 height: auto;
 width: 206px;
  height: auto;
  display: flex;
  align-content: center;
  padding: 6px;
  background: #f7f7f7;
}
.vh-bike {
  margin-right: 20px;
}
.vh-bike,
.vh-car {
  padding: 10px 25px;
  transition: 0.3s;
  border-radius: 4px;
  display: flex;
  align-items: center;
  justify-content: center;
  /* background: #f7f7f7; */
}
/* .vh-bike:hover ,.vh-car:hover{
    background: white;
} */
.bike-bkg {
  background: white;
  -webkit-box-shadow: 0px 0px 7px 1px rgba(163, 163, 163, 0.2);
  -moz-box-shadow: 0px 0px 7px 1px rgba(163, 163, 163, 0.2);
  box-shadow: 0px 0px 7px 1px rgba(163, 163, 163, 0.2);
}
.get-est a {
  padding: 14px 35px;
  background: #8454ff;
  color: white;
  text-decoration: none;
  border-radius: 4px;
  margin-left: 15px;
  font-size: 14px;
  transition: 0.3s;
}
.get-est a:hover{
      -webkit-box-shadow: 0px 5px 45px 1px rgba(132, 84, 255, 0.25);
  -moz-box-shadow: 0px 5px 45px 1px rgba(132, 84, 255, 0.25);
  box-shadow: 0px 5px 45px 1px rgba(132, 84, 255, 0.25);
}
@media screen and (max-width:430px){
  .get-est a{
    padding: 14px 20px;
  }
}
@media screen and (max-width:400px){
  .get-est a{
    padding: 14px 15px;
    font-size: 12px;
  }
}
@media screen and (max-width:3750px){
  .select-vehicle{
    width: 170px;
  }
  .vh-car,.vh-bike{
  padding: 10px 15px;
  }
}
</style>
