<template>
  <div class="f-h how-it-work pad-m" style="position:relative;">
    <div class="container">
      <ridehead
      class="hide-workhead"
        v-for="head in this.datahead"
        :head="head"
        :key="head.key"
        id="work-head"
      />
      <workSlider />
    </div>
    <slider />
  </div>
</template>
<script>
// import howitworkhead from './how-it-work-head';
import workSlider from "./how-it-work-slider";

import ridehead from "./container-head";
import slider from "./how-it-work-slider-bkg";
export default {
  components: {
    ridehead,
    slider,
    workSlider
  },
  data() {
    return {
      datahead: [
        {
          h1: "How does Godrive Work",
          p1: "Just choose the destination with some",
          p2: "simple touches!"
        }
      ]
    }
    
  },
   methods: {
    rideHeadAnimation(pageOffset) {
      var workContainer = document.querySelector(".how-it-work");
      var workHead= document.querySelector("#work-head");
      var workContainerOffsetTop = workContainer.offsetTop;
      var workClientHeight = workContainer.clientHeight;
      var workhalfClientHeight = workClientHeight / 2;
      var res = workContainerOffsetTop - workhalfClientHeight;
      if (pageOffset >= res) {
        workHead.classList.add("animated", "fadeInUp","show-workhead");
          workHead.classList.remove('hide-workhead');
      }
    }
  },
  created() {
    document.addEventListener("DOMContentLoaded", () => {
      window.addEventListener("scroll", () => {
        this.rideHeadAnimation(window.pageYOffset);
      });
    });
  },
  destroyed() {
    window.removeEventListener("scroll", () => {
      this.rideHeadAnimation(window.pageYOffset);
    });
  }
};
</script>
<style scoped>
.mt-1 {
  margin-top: 100px;
}
.show-workhead{
    opacity: 1;
}
.hide-workhead{
    opacity: 0;
}
</style>
