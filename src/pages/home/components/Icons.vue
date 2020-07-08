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
  data () {
    return {
      iconList: [{
        id: '1',
        imgUrl: '//picbed.qunarzz.com/01d2f57f920666364197a850dab859a8.png',
        text: 'hotel'
      }, {
        id: '2',
        imgUrl: '//picbed.qunarzz.com/83af731055e121a3251690b225327b56.png',
        text: 'flight'
      }, {
        id: '3',
        imgUrl: '//picbed.qunarzz.com/5b6737be49ca243072ca614f07803b83.png',
        text: 'train'
      }, {
        id: '4',
        imgUrl: '//picbed.qunarzz.com/1e107321f5396ea4994cd832232ecf8a.png',
        text: 'train'
      }, {
        id: '5',
        imgUrl: '//picbed.qunarzz.com/c65b3bb7571a6bd62df669213e44b84d.png',
        text: 'train'
      }, {
        id: '6',
        imgUrl: '//picbed.qunarzz.com/f6bb08a239ce1b038204120a8d1e4669.png',
        text: 'train'
      }, {
        id: '7',
        imgUrl: '//picbed.qunarzz.com/3a08f360e958ccb2b947049387873ace.png',
        text: 'train'
      }, {
        id: '8',
        imgUrl: '//picbed.qunarzz.com/799d9d090d1625a854194460c8849fee.png',
        text: 'train'
      }, {
        id: '9',
        imgUrl: '//picbed.qunarzz.com/25e3b9f17a21a6e0113c57a23ffccde4.png',
        text: 'hotel'
      }, {
        id: '10',
        imgUrl: '//picbed.qunarzz.com/19b4f6d2fabd617789fa5aad65b249da.png',
        text: 'hotel'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
    .icons
        overflow : hidden
        height : 0
        padding-bottom : 40%
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
