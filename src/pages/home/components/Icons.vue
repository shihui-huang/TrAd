<template>
    <div class="icons">
        <div class="icon" v-for="item of iconList" :key="item.id">
            <div class="icon-img">
                <img class="icon-imgContent" :src="item.imgUrl"/>
            </div>
            <p class="icon-text">{{item.text}}</p>
        </div>
    </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  props: {
    iconList: Array
  }
}
</script>

<style lang="stylus" scoped>
    .icons
        overflow : hidden
        height : 0
        padding-bottom : 29%
        margin-top :.2rem
        .icon
            position :relative
            overflow hidden
            float : left
            width : 20%
            height : 0
            padding-bottom : 15%
            .icon-img
                position :absolute
                height 50%
                top:0
                left :0
                right:0
                margin-bottom : .1rem
                box-sizing: border-box
                .icon-imgContent
                    width : 37%
                    display: block
                    margin: 0 auto
            .icon-text
                position:absolute
                left:0
                right:0
                bottom:0
                height: .35 rem
                line-height: .35 rem
                text-align : center
                color:#333
                margin-bottom :.2rem

</style>
