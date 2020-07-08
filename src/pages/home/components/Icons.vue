<template>
    <div class="icons">
        <div class="icon">
            <div class="icon-img">
                <img class="icon-imgContent" src="//s.qunarzz.com/homenode/images/touchheader/hotel.png"/>
            </div>
            <p class="icon-text">热门景点</p>
        </div>
                <div class="icon">
            <div class="icon-img">
                <img class="icon-imgContent" src="//s.qunarzz.com/homenode/images/touchheader/hotel.png"/>
            </div>
            <p class="icon-text">热门景点</p>
        </div>
                <div class="icon">
            <div class="icon-img">
                <img class="icon-imgContent" src="//s.qunarzz.com/homenode/images/touchheader/hotel.png"/>
            </div>
            <p class="icon-text">热门景点</p>
        </div>
                <div class="icon">
            <div class="icon-img">
                <img class="icon-imgContent" src="//s.qunarzz.com/homenode/images/touchheader/hotel.png"/>
            </div>
            <p class="icon-text">热门景点</p>
        </div>
                <div class="icon">
            <div class="icon-img">
                <img class="icon-imgContent" src="//s.qunarzz.com/homenode/images/touchheader/hotel.png"/>
            </div>
            <p class="icon-text">热门景点</p>
        </div>
        <div class="icon"></div>
        <div class="icon"></div>
        <div class="icon"></div>
        <div class="icon"></div>
        <div class="icon"></div>
        <div class="icon"></div>
        <div class="icon"></div>
    </div>
</template>

<script>
export default {
  name: 'HomeIcons'
}
</script>

<style lang="stylus" scoped>
    .icons
        overflow : hidden
        height : 0
        padding-bottom : 50%
        .icon
            position :relative
            overflow hidden
            float : left
            width : 25%
            height : 0
            padding-bottom : 25%
            .icon-img
                position :absolute
                top:0
                left :0
                right:0
                bottom : .44 rem
                box-sizing: border-box
                padding : .1 rem
                .icon-imgContent
                    display: block
                    height: 100%
                    margin: 0 auto
            .icon-text
                position:absolute
                left:0
                right:0
                bottom:0
                height: .44 rem
                line-height: .44 rem
                text-align : center
                color:#333

</style>
