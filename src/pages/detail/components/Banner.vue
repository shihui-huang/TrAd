<template>
    <div class="banner">
        <img class="banner-img" src="//www.parkgrandlondon.com/blog/wp-content/uploads/2019/04/shutterstock_131155331.jpg"/>
        <div class="banner-info">
            <div class="banner-title">Trafalgar Square - Londre</div>
            <div class="banner-number">
                <span class="iconfont banner-icon"> &#xe692; </span>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'DeatilBanner'
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
