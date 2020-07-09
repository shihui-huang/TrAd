<template>
<div>
    <div class="recommend-title">
        <div class="title-square"> </div>
        <div class="title-text">Where to go on weekends</div>
    </div>
    <ul v-for="item of recommendWeekendList" :key="item.id">
      <li class="border-bottom">
         <div class="item-img-warpper">
            <img class="item-img" :src='item.imgUrl' />
          </div>
          <div class="item-info">
            <p class="item-title">{{item.title}}</p>
            <p class="item-description"> {{item.description}} </p>
        </div>
      </li>
    </ul>
</div>
</template>

<script>
export default {
  name: 'HomeWeekendRecommend',
  data () {
    return {
      recommendWeekendList: [{
        id: '0001',
        title: 'The Louvre reopened !!!',
        description: 'description description',
        imgUrl: '//upload.wikimedia.org/wikipedia/commons/thumb/6/66/Louvre_Museum_Wikimedia_Commons.jpg/280px-Louvre_Museum_Wikimedia_Commons.jpg'
      }, {
        id: '0002',
        title: '2020 OUTDOOR CINEMA IN PARIS',
        description: 'Les festivals de cinéma en plein air reviennent dans toute la région parisienne pour cet été 2020',
        imgUrl: '//parissecret.com/wp-content/uploads/2019/05/GOLEM13.jpg'
      }, {
        id: '0003',
        title: 'L\'Atelier des Lumières',
        description: 'Une création Gianfranco Iannuzzi - Renato Gatto - Massimiliano Siccardi - avec la collaboration musicale de Luca Longobardi',
        imgUrl: '//www.atelier-lumieres.com/sites/ceportail/modules/custom/mtlMegaBan/img/ADL.jpg'
      }, {
        id: '0004',
        title: 'Nice beach',
        description: 'description description',
        imgUrl: '//tribuca.net/img/pictures/2018/08/20180831132507-nice-plage-touriste-web.jpg'
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
        height:.5 rem
        margin-left : .1 rem
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
    .item-img-warpper
        width:100%
        height: 0
        overflow: hidden
        padding-bottom: 33.9%
        .item-img
            width: 100%
            padding-bottom: 33.9%
            background-position:center center
            background-size: cover
            // object-fit: cover
    .item-info
        padding: .1rem
        //min-width: 0 //When there are too much texts, "..." is displayed automatically当文字过多 自动显示“...”
        .item-title
            line-height: .5 rem
            font-size: .32 rem
            ellipsis()
        .item-description
            text-indent : .2 rem
            color: #ccc
            ellipsis()
</style>
