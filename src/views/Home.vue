<template>
  <div class="home">
    <swiper :options="swiperOption" class="swiper">
            <swiper-slide class="swiper-slide">
              <fbg :show="show" :page="page"></fbg>
            </swiper-slide>
            <swiper-slide class="swiper-slide" v-for="(item,index) in carouselArr" :key="index">
              <bg :bgIndex="item" :page="page"></bg>
            </swiper-slide>
            <div class="swiper-pagination"  slot="pagination"></div>
        </swiper>
  </div>
</template>
<script>
// @ is an alias to /src
import bg from '@/components/myswiper-item/index.vue'
import fbg from '@/components/firstPage/index.vue'

var _this
export default {
  name: 'Home',
  beforeCreate() {
    console.log(this)
    _this=this
  },
  data(){
            return {
                page:0,
                swiperOption:{
                    //显示分页
                    pagination: {
                      el: '.swiper-pagination'
                    },
                    //自动轮播
                    autoplay: false,
                    //开启循环模式
                    loop: false,
                    direction : 'vertical',
                    speed:500,
                    mousewheel: true,
                    on: {
                      slideChangeTransitionEnd: function(){
                        //this.page.index = this.activeIndex
                        //console.log(this.activeIndex)
                        //console.log(_this)
                        _this.page=this.activeIndex
                      },
                    }
                },
                carouselArr:[
                  1,2,3,4
                ],
                show:true
            }
        },
        components:{
            bg,
            fbg
        },
        methods: {
          tt(tt){
            this.page.index = tt
          }
        },
}
</script>

<style lang="scss" scoped>
.item{
  height: 100vh;
   overflow: hidden;
}
.swiper{
   height: 100vh;
   overflow: hidden;
}
</style>
