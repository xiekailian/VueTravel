<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl"/>
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
  export default {
    name: 'HomeSwiper',
    data () {
      return {
        swiperOption: {
          pagination: '.swiper-pagination',
          loop:true
        },
        swiperList:[{
          id:'0001',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1806/fc/e47aa3e1c67bbc02.jpg_750x200_0f3eecf8.jpg'
        },{
          id:'0002',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1806/77/f63bd04dd5319602.jpg_750x200_7a9f64f9.jpg'
        }]
      }
    }
  }
</script>

<style lang="stylus" scoped>
  .wrapper>>>.swiper-pagination-bullet-active
    background:#fff
  .wrapper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 27.0%
    background: #eee
    .swiper-img
      width: 100%
</style>
