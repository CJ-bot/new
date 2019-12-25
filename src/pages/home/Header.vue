<template>
    <div class="wrapper">
        <!--  -->
        <swiper :options="swiperOtion">
            <!--  -->
            <swiper-slide v-for="item of swiper" :key="item.id">
                <img :src="item.imgUrl" class="swiper-img">
            </swiper-slide>
            <!--  -->
            <div class="swiper-pagination" slot="pagination"></div>
        </swiper>
    </div>
</template>

<script>
export default {
    name:'HomeHeader',
    data(){
        return{
            swiperOption:{
                pagination:'.swiper-pagination',
                loop:true
            },
            swiperList:[{
                id:'001',
                imgUrl:''
            },{
                id:'002',
                imgUrl:''
            },{
                id:'003',
                imgUrl:''
            },{
                id:'004',
                imgUrl:''
            }]
        }
    }
}
</script>
<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active
  background: #fff
.wrapper
  overflow: hidden
  width: 100%
  height: 0
  padding-bottom: 26.66%
  .swiper-img
      width: 100%
</style>