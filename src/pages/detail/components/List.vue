<template>
  <div>
    <div class="comment">
    <div class="title border-bottom">
      <div class="square"></div>
      <div class="text">Reviews </div>
    </div>
    <div class="commentContents">
      <div class="sigleComment" v-for="item of commentList" :key="item.id">
        <div class="firstLine">
          <div class="stars">
            <div class="star"></div>
            <div class="star"></div>
            <div class="star"></div>
            <div class="star"></div>
            <div class="star"></div>
          </div>
          <div class="date">{{item.name}} {{item.date}}</div>
        </div>
        <div class="commentContentText border-bottom">{{item.content}}</div>
      </div>
    </div>
  </div>
  </div>
</template>

<script>
export default {
  name: 'DetailList',
  props: {
    commentList: Array
  }
}
</script>

<style lang="stylus" scoped>
   @import '~styles/varibles.styl'
  .comment
    margin-top:.2rem
    background: white
    .title
      margin-top: 0.2rem
      margin-left: 0.1rem
      height: 0.5rem
      margin-bottom: 0.2rem
      padding: .1rem
      .square
        width: 0.15rem
        height: 0.5rem
        display: inline
        float: left
        background-color: $bgColor
      .text
        line-height: 0.5rem
        text-indent: 0.2rem
        font-weight: bold
    .commentContents
      margin-left:.2rem
      .firstLine
        display:flex
        text-align:center
        margin-top:.2rem
      .stars
        display:flex
        margin: .1rem
        .star
          width: .2rem
          height: .2rem
          border-radius: .1rem
          background : $bgColor
          margin: .05rem
      .date
        right: 0.5rem;
        position: absolute;
        font-size :small
      .commentContentText
          text-indent: .2rem
          line-height: .4rem
          letter-spacing :0.02rem
          padding-bottom : .2rem
</style>
