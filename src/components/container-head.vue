<template>
    <div class="f-h">
        <div class="ride-head">
        <h1>{{head.h1}}</h1>
        <p>{{head.p1}}</p>
        <p>{{head.p2}}</p>
        </div>
    </div>
</template>
<script>
export default {
  props:['head']
}
</script>
<style scoped>
.ride-head{
    width: 100%;
    height: auto;
text-align: center;
}
.ride-head h1{
    margin-bottom: 25px;
    font-size: 38px;
}
.ride-head p{
    font-size: 14px;
}
</style>
