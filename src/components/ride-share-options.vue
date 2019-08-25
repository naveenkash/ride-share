<template>
    <div class="ride-opt-wrapper">
        <div class="ride-opt">
            <img :src="data.img" alt="">
            <h4>{{data.head}}</h4>
            <p>{{data.text}}</p>
        </div>
    </div>
</template>
<script>
export default {
    props:['data'],
    data(){
        return{

        }
    }
}
</script>
<style scoped>
.ride-opt-wrapper{
    text-align: center;
}
.ride-opt{
    padding:30px 58px;
}
.ride-opt img{
    width: 160px;
    height: 160px;
}
.ride-opt h4{
    margin: 20px 0;
}
.ride-opt p{
    line-height: 30px;
    font-size: 15px;
}
@media screen and (max-width:1050px){
   .ride-opt{
    padding:30px 40px;
} 
}
@media screen and (max-width:900px){
   .ride-opt{
    padding:30px 10px;
} 
}

</style>
