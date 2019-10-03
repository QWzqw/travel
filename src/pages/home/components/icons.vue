<template>
  <div class="icons">
    <swiper :options="swiperOption">
       <swiper-slide v-for="(page,index) of pages" :key="index" >
        <div class="icon" v-for="item in page" :key="item.id">
          <div class="icon-img">
            <img :src='item.imgURl' alt="" class="icon-img-content">
          </div>
          <p class="icon-desc"> {{item.desc}}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        paginationClickable: true,
        autoplayDisableOnInteraction: false
      },
      iconList: [{
        id: '0001',
        imgURl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        desc: '景点门票'
      }, {
        id: '0002',
        imgURl: 'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
        desc: '广州必游'
      }, {
        id: '0003',
        imgURl: 'http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png',
        desc: '动植物园'
      }, {
        id: '0004',
        imgURl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/a40ee278d67000f2a29d2e20f6a029b3.png',
        desc: '自然风光'
      }, {
        id: '0005',
        imgURl: 'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
        desc: '一日游'
      }, {
        id: '0006',
        imgURl: 'http://img1.qunarzz.com/piao/fusion/1803/3e/86314b2af03b7502.png',
        desc: '水上乐园'
      }, {
        id: '0007',
        imgURl: 'http://img1.qunarzz.com/piao/fusion/1803/50/26ffa31b56646402.png',
        desc: '亲子游'
      }, {
        id: '0008',
        imgURl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/bda58ffc3016edad84e656e8a94b0321.png',
        desc: '广州融创'
      }, {
        id: '0009',
        imgURl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/c032ae43b15a3dac34b5e07bb0e46850.png',
        desc: '广州塔'
      }]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style  lang ='stylus' scoped>
  @import '~styles/varibles.styl'
  @import '~styles/mixins.styl'
  .icons>>>.swiper-container
    width : 100%
    height: 0
    padding-bottom : 50%
    .icons
      margin: .2rem
    .icon
      width: 25%
      height: 0
      float: left
      overflow: hidden
      position : relative
      padding-bottom : 25%
      .icon-img
        position: absolute
        top: 0
        left: 0
        right:0
        bottom :0
        box-sizing : border-box
        padding: 0.1rem
        padding-bottom : .44rem
        .icon-img-content
          height :100%
          display :block
          margin :0  auto
      .icon-desc
        position: absolute
        left : 0
        right : 0
        bottom :0
        line-height :.44rem
        color : $daskColor
        text-align : center
        overflow: hidden
        text-overflow: ellipsis
        white-space: nowrap
</style>
