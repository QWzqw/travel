<template>
  <div>
    <div class="recommend-title">周末去哪</div>
    <ul>
      <li class="item border-bottom" v-for="item in recommendList" :key="item.id">
        <div class="item-img-wrraper">
          <img class="item" :src="item.imgUrl" alt="">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'HomeWeenkend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'https://img1.qunarzz.com/sight/p0/1503/4a/4a2ba4bfc1d8d25b.water.jpg_600x330_556f5a2c.jpg',
        title: '珠海海泉湾神秘岛',
        desc: '具有个性魅力的主题乐园'
      }, {
        id: '0002',
        imgUrl: 'https://img1.qunarzz.com/sight/p0/1604/b8/b8e41237b32404d590.img.jpg_600x330_c6059da4.jpg',
        title: '珠海海泉湾神秘岛',
        desc: '具有个性魅力的主题乐园'
      }, {
        id: '0003',
        imgUrl: 'https://img1.qunarzz.com/sight/p0/1803/7e/7ef7350aa26bb843a3.water.jpg_600x330_3fb7cbe9.jpg',
        title: '澳门环岛游',
        desc: '“浪漫之城”珠海的美丽景色一览无余'
      }
      ]
    }
  }
}
</script>
<style lang="stylus" scoped>
@import '~styles/mixins.styl';
  .recommend-title
    line-height: .8rem
    background-color: #eeeeee
    text-indent: .2rem
    margin-top:.2rem
  .item-img-wrraper 
    overflow: hidden
    height : 0;
    padding-bottom :40%
    .item-img
      width:100%
  .item-info
    flex: 1
    padding: .1rem
    min-width: 0
    .item-title
      line-height: .54rem
      font-size: .32rem
      overflow: hidden
      text-overflow: ellipsis
      white-space: nowrap
    .item-desc
      color: #ccc
      line-height: .4rem
      overflow: hidden
      text-overflow: ellipsis
      white-space: nowrap
      margin-bottom: 0.5rem
</style>
