<template>
     <!-- <div class="f-h">  -->
     <!--  <div class="container clearfix"> -->
            <div class="news-info">
                <img :src="data.img" alt="">
                <h4>{{data.head}}</h4>
                <p>{{data.info}}</p>
                <a href="#">Learn More</a>
            </div>
        <!-- </div>-->
    <!-- </div>  -->
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
.news-info {
    width: 50%;
    float: left;
    padding: 20px;
    line-height: 35px;
}
.news-info img{
    width: 100%;
    height: 400px;
}
.news-info h4{
    font-size: 16px;
    margin-top: 10px;
}
.news-info p{
    font-size: 14px;
}
.news-info a{
    text-decoration: none;
    color: rgb(70, 158, 240);
}
@media screen and (max-width:1050px) {
    .news-info img{
    height: 350px;
}
}
@media screen and (max-width:900px) {
    .news-info img{
    height: 300px;
}
}
@media screen and (max-width:800px) {
    .news-info img{
    height: 260px;
}
}

@media screen and (max-width:650px) {
    .news-info{
        width: 100%;
        float: none;
        text-align: center;
} 
 .news-info img{
        width: 350px;
}
}
@media screen and (max-width:440px) {
    .news-info{
        padding: 20px 0 ;
} 
 .news-info img{
        width: 100%;
    height: 240px;
}
}
</style>
