<template>
    <div class="content">
        <div class="header">
            <mnav></mnav>
        </div>
        <div class="text">
            <p class="title">RONG HE</p>
            <transition name="top">
                <p class="textC" v-if="show">致力于成为一家在大数据和社交网络时代为企业智慧经营全面赋能的营销科技公司</p>
            </transition>
            <transition name="top">
                <p class="textE" v-if="show">A marketing technology company dedicated to enhancing our clients’ enterprise capabilities through intelligent management and operation<br> in the era of big data and social networks</p>
            </transition>
        </div>
        <div class="next">
            <img src="@/static/img/arrow-down.png">
        </div>
        <video muted autoplay="autoplay" loop="loop">
            <source src="../../static/img/homepage.mp4" type="video/mp4"/>
        </video>
    </div>
</template>
<script>
import mnav from '@/components/header/index.vue'
export default {
    components:{
        mnav
    },
    data() {
        return {
        }
    },
    props:{
        show:Boolean
    }
}
</script>

<style  scoped>
    .content{
        position: relative;
        width: 100%;
        height: 100vh;
    }
    .header{
        position: absolute;
        left: 0;
        right: 0;
        margin: auto;
    }
    .text{
        position: absolute;
        left: 0;
        right: 0;
        margin: auto;
        text-align: center;
        top:35%;
        color: #fff;
    }
    .text .title{
        font-size: 100px;
        color: #ffffff;
    }
    .textC{
        margin-top: 40px;
        font-size: 24px;
        letter-spacing: 1px;
    }
    .textE{
        font-size: 18px;
        width: 750px;
        margin: 10px auto 0;
    }
    .next{
        position: absolute;
        left: 0;
        right: 0;
        margin: auto;
        width: 56px;
        bottom: 60px;
    }
    .next>img{
        width: 100%;
    }
</style>