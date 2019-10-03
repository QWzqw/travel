<template>
  <div>
    <div class="recommend-title">周末去哪</div>
    <ul>
      <li class="item border-bottom" v-for="item in list" :key="item.id">
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
