<template>
  <div class="f-h pad-m">
      <div class="container">
          <div class="follow-container">
        <ridehead v-for="head in this.datahead" :head="head" :key="head.key"/>
                <rider/>
          </div>
      </div>
  </div>
</template>
<script>
import ridehead from './container-head';
import rider from './rider'
export default {
    components:{
      ridehead,
rider
    },
  data() {
    return {
                  datahead:[{h1:'Follow Your Own Path',p1:'You will have the city at your fingertips  ',p2:'with some simple touches!'}]

    };
  }
};
</script>
<style scoped>
</style>
