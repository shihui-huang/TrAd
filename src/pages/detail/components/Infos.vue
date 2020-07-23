<template>
    <div>
        <div class="info">
            <div class="title" style="padding-top:0"> Overview </div>
            <div class="descriprion border-bottom"> {{this.infos.info}} </div>
            <div class="title"> Open Now </div>
            <div class="descriprion" style="padding-bottom: 0px"> Hours Today : 12:00 AM - 11:59 PM</div>
            <div class="descriprion border-bottom" style="color: #069; cursor: pointer;"> See all hours</div>
            <div class="title"> Suggested Duration: </div>
            <div class="descriprion" style="padding-bottom:0"> {{this.infos.suggestedDuration}}</div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'DetailInfo',
  props: {
    infos: ''
  }
}
</script>

<style lang="stylus" scoped>
  .info
    padding: .4rem
    align-content : center
    justify-content :center
    font-size: 14px
    line-height: 18px
    border-radius : .01rem
    background : white
    margin-top: .2rem
    .title
      padding: .15rem 0rem
      font-size: .32rem
      line-height: 20px
      color: #474747
    .descriprion
      color:#aaa
      padding-bottom: 10px
      text-indent :.2rem
</style>
