<template>
   <div class="search">
       <input class="search-input" type="text" placeholder="Enter a city name"/>
   </div>
</template>

<script>
export default {
  name: 'CitySearch'
}
</script>

<style lang="stylus" scoped>
    @import '~styles/varibles.styl'
    .search
        height : .72 rem
        padding : 0 0.1rem
        background : $bgColor
        .search-input
            box-sizing: border-box
            width : 100%
            height : .62 rem
            padding : 0.1 rem
            line-height : .62 rem
            text-align : center
            border-radius: .06 rem
            color: #666
</style>
