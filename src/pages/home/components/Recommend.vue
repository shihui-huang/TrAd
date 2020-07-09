<template>
<div>
    <div class="recommend-title">
        <div class="title-square"> </div>
        <div class="title-text">Popular sites</div>
    </div>
    <ul v-for="item of recommendList" :key="item.id">
      <li class="item border-bottom">
          <img class="item-img" :src='item.imgUrl' />
          <div class="item-info">
            <p class="item-title">{{item.title}}</p>
            <p class="item-description"> {{item.description}} </p>
            <button class="item-button">detail</button>
        </div>
      </li>
    </ul>
</div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        title: 'The Royal Horseguards',
        description: 'description description',
        imgUrl: '//media-cdn.tripadvisor.com/media/photo-s/1b/45/12/3c/exterior.jpg'
      }, {
        id: '0002',
        title: 'The Royal Horseguards',
        description: 'description description',
        imgUrl: '//media-cdn.tripadvisor.com/media/photo-s/1b/45/12/3c/exterior.jpg'
      }, {
        id: '0003',
        title: 'The Royal Horseguards',
        description: 'description description',
        imgUrl: '//media-cdn.tripadvisor.com/media/photo-s/1b/45/12/3c/exterior.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl'
@import '~styles/varibles.styl'
  .recommend-title
    margin-top: .2 rem
    margin-left : .1 rem
    height:.5 rem
    justify-item : center
    margin-bottom : .2 rem
    .title-square
        width: 0.15 rem
        height : .5 rem
        display : inline
        float :left
        background-color:$bgColor
    .title-text
        line-height :.5 rem
        text-indent: .2 rem
        font-weight: bold
  .item
    display :flex
    height :1.9 rem
    overflow : hidden
    .item-img
      width : 1.7 rem
      height : 1.7 rem
      padding : .1rem
    .item-info
        flex:1
        padding: .1 rem
        min-width: 0 //When there are too much texts, "..." is displayed automatically当文字过多 自动显示“...”
      .item-title
        line-height : .54 rem
        font-size : .32 rem
        ellipsis()
      .item-description
        line-height: .4 rem
        color: #ccc
        ellipsis()
      .item-button
        width : .80 rem
        font-size : .25 rem
        line-height : .40 rem
        margin-top : .16 rem
        background : $bgColor
        padding: 0 .2 rem
        border-radus: .06 rem
        color: #fff
</style>
