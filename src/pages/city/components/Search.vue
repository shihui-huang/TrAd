<template>
    <div>
        <div class="search">
            <input v-model="keyword"
            class="search-input"
            type="text"
            placeholder="Enter a city name"
            onfocus="this.placeholder=''"
            onblur="this.placeholder='Enter a city name'"/>
        </div>
        <div class="search-content" ref='search' v-show='keyword '>
            <ul>
                <li class="search-item border-bottom" v-for="item of list" :key="item.name" @click="handleCityClick(item.name)">{{item.name}}</li>
                <li class="search-item border-bottom" v-show="hasNoList"> There is no matching city </li>
            </ul>
        </div>
    </div>
</template>

<script>
import Bscroll from 'better-scroll'
import { mapMutations } from 'vuex'
export default {
  name: 'CitySearch',
  props: {
    cityList: {}
  },
  data () {
    return {
      keyword: '',
      list: [],
      timer: null
    }
  },
  methods: {
    handleCityClick (city) {
      // this.$store.commit('changeCity', city)
      this.changeCity(city)
      this.$router.push('/')
      this.keyword = ''
    },
    ...mapMutations(['changeCity'])
  },
  computed: {
    hasNoList () {
      return !this.list.length
    }
  },
  watch: {
    keyword () {
      if (this.timer) {
        clearTimeout(this.timer)
      }
      if (!this.keyword) {
        this.list = []
        return
      }
      this.timer = setTimeout(() => {
        let result = []
        for (let i in this.cityList) {
          this.cityList[i].forEach(element => {
            if ((element.name.toUpperCase().indexOf(this.keyword.toUpperCase())) > -1) {
              result.push(element)
            }
          })
        }
        this.list = result
      }, 100)
    }
  },
  mounted () {
    this.scroll = new Bscroll(this.$refs.search)
  }
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
    .search-content
        z-index: 1
        overflow: hidden
        position: absolute
        top: 1.58rem
        left : 0
        right: 0
        bottom: 0
        background :#eee
        .search-item
          line-height: .62rem
          padding-left: .2rem
          background: #fff
          color : #666
</style>
