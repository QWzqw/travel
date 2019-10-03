<template>
  <div class="wrraper">
      <swiper :options="swiperOption" >
      <!-- slides -->
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" />
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination"  slot="pagination"></div>
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
        autoplay: 3000,
        loop: true
      },
      swiperList: [ {
        id: '0001',
        imgUrl: 'https://s.qunarzz.com/m_bus_search/images/banner_defaut.png'
      }, {
        id: '0002',
        imgUrl: 'http://dimg04.c-ctrip.com/images/700h0i0000009nvq206D5_750_330_217.jpg'
      }
      ]
    }
  }
}
</script>
<style lang="stylus" scoped >
.wrraper >>> .swiper-pagination-bullet-active
  background-color : #fff
.wrraper
  overflow : hidden
  width :100%
  height :0
  padding-bottom :42%
  .swiper-img
    width:100%
    background-color:#eee
</style>
