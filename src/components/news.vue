<template>
    <div class="f-h pad-m news-bkg">
        <div class="container">
            
            <ridehead v-for="head in this.datahead" :head="head" :key="head.key"/>
            <div class="news-con pad-t">
            <newsInfo v-for="data in newsdata" :data="data" :key="data.key"/></div>
        </div>
       
    </div>
</template>
<script>
import ridehead from './container-head';
import newsInfo from './news-info'
export default {
     components:{
        ridehead,
        newsInfo
    },
    data(){
        return{
             datahead:[{h1:'Latest News',p1:'Be updated with latest news for exciting ',p2:'prizes,coupons and many more!'}],
             newsdata:[{img:'https://react-next-landing.redq.io/_next/static/images/blog-1-5700c118c247382c19adecc89d3b9949.svg',head:'Built for drivers, with drivers',info:'The new Driver app helps you earn smarter and supports you–like a partner–at every turn.'},
             {img:'https://react-next-landing.redq.io/_next/static/images/blog-2-6d408e493422840dc6983501beb22797.svg',head:'Bike Share',info:'All the Riders have been verified by us. Not random people with bikes that we don’t know.'}]
        }
    }
   
}
</script>
<style scoped>
.news-con{
    display: flex;
    flex-wrap: wrap;
}
.news-bkg{
    background: #FCFCFC;
}

</style>
