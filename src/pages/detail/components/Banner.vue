<template>
    <div>
        <div class="banner" @click="handleBannerClick" >
            <img class="banner-img" :src="img"/>
            <div class="banner-info">
                <div class="banner-title">{{name}}</div>
                <div class="banner-number">
                    <span class="iconfont banner-icon"> &#xe692; </span>
                </div>
            </div>
        </div>
          <common-gallary :imgs="imgs" v-show="showGallary" @disappear="cancelBannerClick"></common-gallary>
    </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DeatilBanner',
  props: {
    imgs: Array,
    name: String
  },
  data () {
    return {
      showGallary: false
    }
  },
  computed: {
    img () {
      return this.imgs[0]
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    cancelBannerClick () {
      this.showGallary = false
    }
  },
  components: {
    CommonGallary
  }
}
</script>

<style lang="stylus" scoped>
    .banner
        position: relative
        overflow: hidden
        height: 0
        padding-bottom: 55%
        .banner-img
            width: 100%
        .banner-info
            display: flex
            position: absolute
            left: 0
            right: 0
            bottom: 0
            line-height: .7rem
            color: #fff
            background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8))
            .banner-title
                font-size: .30rem
                padding: 0 .2rem
            .banner-number
                right: .3rem
                height: .32rem
                line-height: .32rem
                margin-top: .14rem
                padding: 0 .4rem
                border-radius: .2rem
                background: rgba(0, 0, 0, .8)
                font-size: .24rem
                position: absolute
                .banner-icon
                    font-size: .24rem
</style>
