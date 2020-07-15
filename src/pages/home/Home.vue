<template>
  <div>
    <home-header ></home-header>
    <home-swiper :swiperList="swiperList"></home-swiper>
    <home-icons :iconList="iconList"></home-icons>
    <home-recommend :recommendList="recommendList" ></home-recommend>
    <home-weekend-recommend :recommendWeekendList="recommendWeekendList"></home-weekend-recommend>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import HomeRecommend from './components/Recommend'
import HomeWeekendRecommend from './components/Weekend'
import axios from 'axios'
import { mapState } from 'vuex'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeRecommend,
    HomeWeekendRecommend
  },
  data () {
    return {
      swiperList: [],
      iconList: [],
      recommendList: [],
      recommendWeekendList: [],
      lastCity: ''
    }
  },
  computed: {
    ...mapState(['city'])
  },
  methods: {
    getHomeInfo () {
      axios.get('/static/mock/index.json?city=' + this.city)
        .then(this.getHomeInfoSucc)
    },
    getHomeInfoSucc (res) {
      res = res.data
      if (res.ret && res.data) {
        // If the backend returns the result correctly 如果后端正确返回了结果且res里有data
        const data = res.data
        this.swiperList = data.swiperList
        this.iconList = data.iconList
        this.recommendList = data.recommendList
        this.recommendWeekendList = data.recommendWeekendList
      }
    }
  },
  mounted () {
    this.lastCity = this.city
    this.getHomeInfo()
  },
  // 当我们使用keep-alive时会多处一个生命周期函数activated
  // When we use keep-alive, there will be one more life cycle function: activated
  // mounted 是第一次加载时会触发 activated是每一次回到home页都时候都会触发
  // mounted is triggered when it is loaded for the first time. activated is triggered every time it returns to the home page
  activated () {
  // 每次加载去判断当前城市是否和上一次都一样 若不一样再发一次ajax请求
  // Every time you load to determine whether the current city is the same as the last time, if it is not the same, send another ajax request
    if (this.lastCity !== this.city) {
      this.lastCity = this.city
      this.getHomeInfo()
    }
  }
}
</script>

<style >

</style>
