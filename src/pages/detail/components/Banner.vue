<template>
    <div>
        <div class="banner" @click="handleBannerClick" >
            <img class="banner-img" src="//www.parkgrandlondon.com/blog/wp-content/uploads/2019/04/shutterstock_131155331.jpg"/>
            <div class="banner-info">
                <div class="banner-title">Trafalgar Square - Londre</div>
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
  data () {
    return {
      showGallary: false,
      imgs: ['//www.willpearson.co.uk/wp-content/uploads/2013/04/trafalgar-square-panorama.jpg',
        '//www.parkgrandlondon.com/blog/wp-content/uploads/2016/07/shutterstock_140801782.jpg',
        '//www.parkgrandlondon.com/blog/wp-content/uploads/2017/02/shutterstock_617406509.jpg']
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
