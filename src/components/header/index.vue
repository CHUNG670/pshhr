<template>
    <div>
        <div class="nav">
            <div class="logo">
                <img src="@/static/img/logo.png" alt="" srcset="">
            </div>
            <ul>
                <li>关于榕河</li>
                <li>核心业务</li>
                <li>新闻中心</li>
                <li>营销软件</li>
                <li>作品介绍</li>
                <li>联系我们</li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {}

</script>

<style scope>
    .logo{
        width: 131px;
        display: inline-block;
        vertical-align: middle;
    }
    .logo img{
        width: 100%;
    }
    .nav{
        width: 1200px;
        margin: 0 auto;
        display: flex;
        align-content: center;
        padding-top: 50px;
        box-sizing: border-box;
    }
    .content{
        width: 100%;
    }
    li{
        list-style:none;
        float: left;
        color: #fff;
        opacity: .5;
        font-size: 14px;
        text-decoration: none;
        margin: 0 20px;
    }
    ul{
        display: inline-block;
        overflow: hidden;
        vertical-align: middle;
        display: flex;
        align-items: center;
        margin-left: 80px;

    }
</style>