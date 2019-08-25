<template>
  <div class="f-h by-ride pad-m">
    <div class="container">
      <ridehead v-for="head in this.datahead" :head="head" :key="head.key" />
      <div class="f-h pad-t hide-ride ride-container">
        <rideopt :key="data.key" v-for="data in this.data" :data="data" />
      </div>
    </div>
  </div>
</template>
<script>
import rideopt from "./ride-share-options";
import ridehead from "./container-head";
export default {
  components: {
    ridehead,
    rideopt
  },
  data() {
    return {
      data: [
        {
          img: require("../assets/rider1-svg.svg"),
          text:
            "Documents, accessories, packages and even gifts! Deliver them all within your city, in a jiffy!",
          head: "Delivery"
        },
        {
          img: require("../assets/rider2-svg.svg"),
          text:
            "All the Riders have been verified by us. Not random people with bikes that we don’t know.",
          head: "Bike Share"
        },
        {
          img: require("../assets/rider3-svg.svg"),
          text:
            "Order food from your favorite Place near you with the convenience of Godrive.",
          head: "Food"
        }
      ],
      datahead: [
        {
          h1: "Beyond Ridesharing",
          p1: "Certain requirements and features vary by ",
          p2: "country, region, and city.!"
        }
      ]
    };
  },
  methods: {
    addAnimation(pageOffset) {
      var rideContainer = document.querySelector(".by-ride");
      var ridewrapper = document.querySelector(".ride-container");
      var rideContainerOffset = rideContainer.offsetTop;
      var rideClientHeight = rideContainer.clientHeight;
      var halfClientHeight = rideClientHeight / 2;
      var res = rideContainerOffset - halfClientHeight;
      if (pageOffset >= res) {
        ridewrapper.classList.add("animated", "fadeInUp","show-ride");
          ridewrapper.classList.remove('hide-ride');
      }
    }
  },
  created() {
    document.addEventListener("DOMContentLoaded", () => {
      window.addEventListener("scroll", () => {
        this.addAnimation(window.pageYOffset);
      });
    });
  },
  destroyed() {
    window.removeEventListener("scroll", () => {
      this.addAnimation(window.pageYOffset);
    });
  }
};
</script>

<style scoped>
.ride-container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
}
.hide-ride{
    opacity: 0;
}
.show-ride{
    opacity: 1;
}
@media screen and (max-width:700px){
  .ride-container{
      grid-template-columns: 1fr 1fr;
  }
}
@media screen and (max-width:500px){
  .ride-container{
      grid-template-columns: 1fr;
  }
}
</style>
