<template>
    <div class="bg1-content">
        <div class="bg1-item" v-for="(item,index) in dataList" :key="index">
            <transition name="fade">
                <div class="line-1">
                    <span>{{item.before}}</span>
                    <sapn class="iCountUp"><ICountUp :endVal="item.data" :options="options" @ready="onReady"/></sapn>
                    <span>{{item.unit}}</span>
                </div>
            </transition>
            <transition name="top2">
                <div class="line-2">
                    {{item.title}}
                </div>
            </transition>
            <transition name="top">
                <div class="line-3">
                    {{item.english}}
                </div>
            </transition> 
        </div>
    </div>
</template>

<script>
import ICountUp from 'vue-countup-v2';
export default {
    data() {
        return {
            dataList:[
                {
                    data:291,
                    title:'年度营收入',
                    english:'Annual Revenue',
                    unit:'亿',
                    before:'￥'
                },
                 {
                    data:5000,
                    title:'公司员工',
                    english:'Employees',
                    unit:'人',
                    before:''
                },
                 {
                    data:59,
                    title:'全球办公室',
                    english:'Worldwide Offices',
                    unit:'个',
                    before:''
                },
                 {
                    data:3000,
                    title:'服务客户',
                    english:'Clients',
                    unit:'+',
                    before:''
                },
                 {
                    data:90,
                    title:'数字化业务营收占比',
                    english:'Digital Related Business (%)',
                    unit:'%',
                    before:''
                },
                 {
                    data:29,
                    title:'国内员工平均年龄',
                    english:'The Average Age of Employees in Mainland China',
                    unit:'岁',
                    before:''
                },
            ],
            options: {
            useEasing: true,
            useGrouping: true,
            separator: '',
            decimal: '.',
            prefix: '',
            suffix: ''
            }
        }
    },
    components:{
        ICountUp
    },
    methods: {
      onReady: function(instance, CountUp) {
        //const that = this;
        //instance.update(that.endVal + 100);
      }
    }

}
</script>

<style scope>
    .bg1-content{
        width: 100%;
        height: 100vh;
        display: flex;
        flex-wrap: wrap;
    }
    .bg1-item{
        width: 33.33%;
        height: 50%;
        color: #fff;
        display: flex;
        justify-content: center;
        flex-direction: column;
        align-items: center;
    }
    .iCountUp{
        font-size: 70px;
        font-family: "DIN";
    }
    .line-1{
        font-size: 24px;
    }
    .line-2{
        font-size: 22px;
    }
     .line-3{
        font-size: 12px;
    }
</style>