<template>
    <div :class="{bg1:bgIndex==1,bg2:bgIndex==2,bg3:bgIndex==3,bg4:bgIndex==4}" class="img-content">
        <div v-if="bgIndex==1">
            <bgone v-if="page==1"></bgone>
        </div>
    </div>
</template>

<script>
import bgone from './components/index-bg1.vue'
export default {
    data() {
        return {
            thispage:0
        }
    },
    props:{
        bgIndex:{
            default:1,
            type:Number
        },
        page:Number
    },
    mounted() {
        
    },
    watch: {
       page(news){
           
           //console.log(news)
       } 
    },
    components:{
       bgone
    }
}
</script>

<style scope>
.img-content{
    width: 100%;
    height: 100vh;
    background-size: cover;
}
.bg1{
    background-image: url('../../static/img/bg1.jpg');
}
.bg2{
    background-image: url('../../static/img/bg2.jpg');
}
.bg3{
    background-image: url('../../static/img/bg3.jpg');
}
.bg4{
    background-image: url('../../static/img/bg4.jpg');
}
.text{
    font-size: 100px;
    color: #ffffff;
}
</style>