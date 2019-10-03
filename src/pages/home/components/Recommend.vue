<template>
  <div>
    <div class="recommend-title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item in list" :key="item.id">
          <img class="item" :src="item.imgUrl" alt="">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-btn">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'HomeRecommend',
  props: {
    list: Array
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
  .item
    overflow: hidden
    display: flex
    height: 1.9rem
    margin: 0.1rem
    .item-img
      height: 1.7rem
      width:1.7rem
      margin: .1rem
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
      .item-btn
        background-color: #ff9300
        padding: 0.02rem .2rem
        border-radius: 0.06rem
        color:#fff
        margin-top: .16rem
        line-height: .44rem

</style>
