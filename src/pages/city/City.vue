<template>
<div>
    <city-header></city-header>
    <city-search :cityList="cityList"></city-search>
    <city-list :cityList="cityList" :popularCityList="popularCityList" :letter="letter"></city-list>
    <city-alphabet :cityList="cityList" @change="handleLetterChange"></city-alphabet>
</div>
</template>

<script>
import axios from 'axios'
import CityHeader from './components/Header'
import CitySearch from './components/Search'
import CityList from './components/List'
import CityAlphabet from './components/Alphabet'
export default {
  name: 'City',
  components: {
    CityHeader,
    CitySearch,
    CityList,
    CityAlphabet
  },
  data () {
    return {
      cityList: [],
      popularCityList: [],
      letter: String
    }
  },
  methods: {
    getCityInfo () {
      axios.get('/static/mock/city.json')
        .then(this.getCityInfoSucc)
    },
    getCityInfoSucc (res) {
      res = res.data
      if (res.ret && res.data) {
        const data = res.data
        this.cityList = data.cityList
        this.popularCityList = data.popularCityList
      }
    },
    handleLetterChange (e) {
      this.letter = e
    }
  },
  mounted () {
    this.getCityInfo()
  }
}
</script>

<style lang="stylus" scoped>

</style>
