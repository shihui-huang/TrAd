<template>
  <div class="header">

    <div class="header-left">
      <span class="iconfont"> &#xe624; </span>
    </div>
    <div class="header-input">
       <span class="iconfont"> &#xe632; </span>
       Where are you going ?
    </div>
    <router-link to='city'>
    <div class="header-right" >
      <div class="text">{{this.city}} </div>
      <div class="iconfont arrow-icon"> &#xe64a; </div>
    </div>
    </router-link>

  </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  name: 'HomeHearder',
  computed: {
    ...mapState(['city'])
  }
}
</script>
// 1rem = 50px

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
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
      margin-left: .2rem
      height: .86 rem
      width: 1.24 rem
      line-height : .86 rem
      float: left
      text-align: center
      color: white
      .text
        overflow: hidden;
        height: 0.86rem;
        float: left;
        width: 0.7rem;
      .arrow-icon
        height: 0.86rem;
        float: left;
        width: 0.2rem;
        margin-left: 0.1rem;
        font-size: 0.22rem;
</style>
