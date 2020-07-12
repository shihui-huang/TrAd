<template>
    <div class='header'>
        Choose city
        <router-link to="/">
            <div class="header-left">
                <span class="iconfont"> &#xe624; </span>
            </div>
        </router-link>
    </div>
</template>

<script>
export default {
  name: 'CityHeader'
}
</script>

<style lang="stylus" scoped>
    @import '~styles/varibles.styl'
    .header
        background-color : $bgColor
        height : $headerHeight
        line-height :$headerHeight
        text-align : center
        color : #fff
        font-size : .32 rem
        overflow : hidden
        position : relative
        .header-left
            position : absolute
            top: 0
            left : 0
            width .64 rem
            color : #fff
            line-height : .86 rem
            float: left
            text-align: center
</style>
