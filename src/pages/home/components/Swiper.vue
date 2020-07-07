<template>
<div class="wrapper">
 <swiper :options="swiperOption">
    <!-- slides -->
    <swiper-slide><img class="swiper-img" src="//imgs.qunarzz.com/vc/6d/9f/35/b8ad5468f73fd60ec0ced086f6.jpg_92.jpg"/></swiper-slide>
    <swiper-slide><img class="swiper-img" src="//imgs.qunarzz.com/vc/e3/a1/71/f498dfd3bed948d623c9093252.jpg_92.jpg"/></swiper-slide>
    <swiper-slide><img class="swiper-img" src="//imgs.qunarzz.com/vs_ceph_vcimg/b8c4527c41649814cc4cf86880abba54.jpeg"/></swiper-slide>

  <!-- <swiper-slide>I'm Slide 3</swiper-slide>
    <swiper-slide>I'm Slide 4</swiper-slide>
    <swiper-slide>I'm Slide 5</swiper-slide>
    <swiper-slide>I'm Slide 6</swiper-slide>
    <swiper-slide>I'm Slide 7</swiper-slide> -->
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
        pagination: '.swiper-pagination'
      }
    }
  }
}
</script>

<style lang="stylus" scoped>
    .wrapper >>> .swiper-pagination-bullet-active // In order not to be restricted by scope
        background :#fff
    .wrapper
        height : 0
        overflow : hidden
        width : 100%
        background:#eee
        padding-bottom : 31.25% //Aspect ratio adaptive图片宽高比自适应
        .swiper-img
            width : 100%
</style>
