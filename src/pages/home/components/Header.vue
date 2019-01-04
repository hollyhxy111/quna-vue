<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入城市/景点/游玩主题</div>
    <div class="header-right">
      {{city}}
      <span class="iconfont arrow-icon">&#xe600;</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHead',
  props: {
    city: String
  }
}
</script>

<style lang='stylus' scoped>
@import '~styles/varibles.styl'
// @import '~@/assets/styles/varibles.styl'
.header
  display: flex
  height: 43px
  background-color: $bgColor
  color: #fff
  .header-left
    width: 32px
    line-height: 43px
    float: left
    .back-icon
      text-align: center
  .header-input
    flex: 1
    height: 32px
    line-height: 32px
    margin-top: 6px
    margin-left: 2px
    padding-left: 5px
    background-color: #fff
    border-radius: 5%
    color: #ccc
  .header-right
    width: 62px
    line-height: 43px
    float: right
    text-align: center
    .arrow-icon
      font-size: 12px
      margin-left: -2px

</style>
