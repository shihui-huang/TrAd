<template>
  <div class="header">
    <div class="header-left">return</div>
    <div class="header-input">Where are you going</div>
    <div class="header-right">City</div>
  </div>
</template>

<script>
export default {
  name: 'HomeHearder'
}
</script>
// 1rem = 50px

<style lang="stylus" scoped>
  .header
    display: flex
    height: .86 rem
    background : #00bcd4
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
      margin-top : .12 rem
      margin-left : .2 rem
      background:#fff
      border-radius: .1 rem
      color : #ccc
    .header-right
      width: 1.24 rem
      line-height : .86 rem
      float: right
      text-align: center

</style>
