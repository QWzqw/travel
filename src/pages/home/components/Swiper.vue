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
        imgUrl: 'https://tr-osdcp.qunarzz.com/tr-osd-tr-manager/img/eff4eb8be47786f9541b3666e240f2cc.jpg'
      }, {
        id: '0002',
        imgUrl: 'https://tr-osdcp.qunarzz.com/tr-osd-tr-manager/img/aad9b1b0ddf1a6432a54e2283cb4f3ca.jpg'
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
  padding-bottom :51%
  .swiper-img
    width:100%
    background-color:#eee
</style>
