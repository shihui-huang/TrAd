<template>
  <div class="header">

    <div class="header-left">
      <span class="iconfont"> &#xe624; </span>
    </div>
    <div class="header-input">
       <span class="iconfont"> &#xe632; </span>
       Where are you going ?
    </div>
    <div class="header-right">City
      <span class="iconfont" arrow-icon> &#xe64a; </span>
    </div>

  </div>
</template>

<script>
export default {
  name: 'HomeHearder'
}
</script>
// 1rem = 50px

<style lang="stylus" scoped>
  @import '~@/assets/styles/varibles.styl'
  .header
    display: flex
    height: .86 rem
    background : $bgColor
    color:#fff
    .header-left
      width .64 rem
      line-height : .86 rem
      float: left
      text-align: center
    .header-input
      flex:1
      height : .64 rem
      line-height : .64 rem
      margin-top : .11 rem
      margin-left : .2 rem
      background:#fff
      border-radius: .1 rem
      color : #ccc
      padding-left : .2 rem
    .header-right
      width: 1.24 rem
      line-height : .86 rem
      float: right
      text-align: center
      .arrow-icon
        margin-left : .2 rem
        font-size : .2 rem
</style>
