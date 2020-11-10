<template>
    <div :class="{bg1:bgIndex==1,bg2:bgIndex==2,bg3:bgIndex==3,bg4:bgIndex==4}" class="img-content">
        
    </div>
</template>

<script>
export default {
    data() {
        return {
            
        }
    },
    props:{
        bgIndex:{
            default:1,
            type:Number
        }
    },
    mounted() {
        
    },
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

</style>