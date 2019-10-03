<template>
  <div class="header ">
        <div class="header-left">
          <div class="iconfont back-icon">&#xe641;</div>
        </div>
        <div class="header-input">
          <span class="iconfont">&#xe724;</span>
          输入城市/景点/默认主题
        </div>
        <div class="header-right">
         {{this.city}}
          <span class="iconfont arrow-icon">&#xe612;</span>
        </div>
  </div>
</template>
<script>
export default{
  name: 'HomeHeader',
  props: {
    city: String
  }
}
</script>
<style lang="stylus" scoped>
@import '~styles/varibles.styl'
  .header
    display: flex
    line-height: 0.86rem
    background-color: $bgColor;
    .header-left
      width: 0.64rem
      float: left
      color: #fff
      text-align: center
      .back-icon
        font-size : 0.4rem
    .header-input
      flex: 1
      background-color: #fff
      margin-top: .12rem
      margin-left : .2rem
      padding-left :0.2rem
      height: 0.64rem
      border-radius:.1rem
      line-height:.64rem
      color:#ccc
    .header-right
      width: 1.24rem
      float: right
      text-align :center
      color: #fff
      .arrow-icon
        font-size :0.4rem
</style>
