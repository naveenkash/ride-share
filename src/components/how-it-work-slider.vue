<template>
  <div class="f-h pad-t">
    <div class="slider-con">
      <div ref="sliderMain" class="slider-img">
        <div ref="sliderChild" class="slider-img-container">
          <div class="slider-img-wrapper">
            <img src="../assets/slider-img1.png" alt />
          </div>
          <div class="slider-img-wrapper">
            <img src="../assets/bike-location.png" alt />
          </div>
          <div class="slider-img-wrapper">
            <img src="../assets/slider-img1.png" alt />
          </div>
          <div class="slider-img-wrapper">
            <img src="../assets/bike-location.png" alt />
          </div>
          <div class="slider-img-wrapper">
            <img src="../assets/slider-img1.png" alt />
          </div>
          <div class="slider-img-wrapper">
            <img src="../assets/slider-img1.png" alt />
          </div>
        </div>
      </div>
      <div class="phn-top">
        <div class="phn-mic"></div>
        <div class="phn-cam"></div>
      </div>
    </div>
    <div class="f-h">
      <div class="slider-btn">
        <div @click="sliderMethod1" :class="{active:dot1}" class="btn1"></div>
        <div @click="sliderMethod2" :class="{active:dot2}" class="btn1"></div>
        <div @click="sliderMethod3" :class="{active:dot3}" class="btn1"></div>
        <div @click="sliderMethod4" :class="{active:dot4}" class="btn1"></div>
        <div @click="sliderMethod5" :class="{active:dot5}" class="btn1"></div>
        <div @click="sliderMethod6" :class="{active:dot6}" class="btn1"></div>
      </div>
    </div>
    <!-- <sliderButton /> -->
  </div>
</template>
<script>
// var lastx = 0;
import { mapActions, mapGetters } from "vuex";
var intervalId;
export default {
  components: {
    // slider
  },
  data() {
    return {
      lastx: 0,
      dot1: false,
      dot2: false,
      dot3: false,
      dot4: false,
      dot5: false,
      dot6: false
    };
  },
  methods: {
    sliderMethod1() {
      this.goToPosition(0);
    },
    sliderMethod2() {
      this.goToPosition(16.6666666667);
    },
    sliderMethod3() {
      this.goToPosition(33.3333333333);
    },
    sliderMethod4() {
      this.goToPosition(50);
    },
    sliderMethod5() {
      this.goToPosition(66.6666666667);
    },
    sliderMethod6() {
      this.goToPosition(83.3333333333);
    },
    goToPosition(pos) {
      this.lastx = pos;
      // console.log("gotoposition" + pos);
      var slider = this.$refs.sliderMain;
      slider.style.transform =
        "translatex" + "(" + "-" + this.lastx + "%" + ")";
      this.refreshedDots();
    },
    refreshedDots() {
      this.dot1 = false;
      this.dot2 = false;
      this.dot3 = false;
      this.dot4 = false;
      this.dot5 = false;
      this.dot6 = false;
      if (this.lastx >= 83.3333333333) {
        this.dot6 = true;
      } else if (this.lastx >= 66.6666666667) {
        this.dot5 = true;
      } else if (this.lastx >= 50) {
        this.dot4 = true;
      } else if (this.lastx >= 33.3333333333) {
        this.dot3 = true;
      } else if (this.lastx >= 16.6666666667) {
        this.dot2 = true;
      } else if (this.lastx >= 0) {
        this.dot1 = true;
      }
    }
  },

  created() {
    // this.setTransformValue(0);
    document.addEventListener("DOMContentLoaded", () => {
      intervalId = setInterval(() => {
        var slider = this.$refs.sliderMain;
        if (this.lastx >= 83) {
          this.goToPosition(0);
        } else {
          this.goToPosition(this.lastx + 16.6666666667);
        }
        //  this.refreshedDots();
      }, 2500);
    });
  },
  beforeDestroy() {
    clearInterval(intervalId);
  }
};
</script>
<style scoped>
.slider-con {
  height: 770px;
  width: 375px;
  margin: 0 auto;
  background: transparent;
  border-radius: 50px;
  /* padding: 15px; */
  /* padding-right: 10px; */
  overflow: hidden;
  z-index: 1;
  border: 13px solid white;
  -webkit-box-shadow: 0px 0px 65px 0px rgba(232, 230, 244, 1);
  -moz-box-shadow: 0px 0px 65px 0px rgba(232, 230, 244, 1);
  box-shadow: 0px 0px 65px 0px rgba(232, 230, 244, 1);
  position: relative;
}
.phn-top {
  position: absolute;
  top: 0;
  left: 25%;
  height: 30px;
  width: 180px;
  background: white;
  border-bottom-left-radius: 20px;
  border-bottom-right-radius: 20px;
  z-index: 100;
}
.phn-mic {
  position: absolute;
  bottom: 10px;
  left: 50%;
  width: 50px;
  height: 5px;
  background: #eceaf9;
  border-radius: 5px;
  transform: translate(-50%, -50%);
}
.phn-cam {
  position: absolute;
  bottom: 4px;
  left: 75%;
  width: 12px;
  height: 12px;
  background: #eceaf9;
  border-radius: 40%;
  transform: translate(-50%, -50%);
}

.slider-img {
  width: 600%;
  height: 100%;
  overflow: hidden;
  transition: all 0.5s;
  transform: translatex(0);
}

.slider-img-container {
  width: 100%;
  height: 100%;
  border-radius: 40px;
  overflow: hidden;
  display: flex;
}
.slider-img-wrapper {
  width: 100%;
  height: 100%;
  overflow: hidden;
}
.slider-img-wrapper img {
  width: 100%;
  height: 100%;
}
.slider-btn {
  width: 100%;
  height: auto;
  display: flex;
  align-items: center;
  text-align: center;
  justify-content: center;

  margin-top: 40px;
}
.btn1 {
  width: 13px;
  height: 13px;
  border-radius: 50%;
  background: #f3f2fb;
  z-index: 1;
  cursor: pointer;
  margin-right: 10px;
  border: 3px solid white;
  -webkit-box-shadow: 0px 1px 2px 0px rgba(0, 0, 0, 0.3);
  -moz-box-shadow: 0px 1px 2px 0px rgba(0, 0, 0, 0.3);
  box-shadow: 0px 1px 2px 0px rgba(0, 0, 0, 0.3);
}
.active {
  background: #8454ff;
}
@media screen and (max-width:500px) {
  .slider-con{
    width: 320px;
    height: 720px;
  }
  .phn-top{
  left: 21%;
  }
}
</style>
