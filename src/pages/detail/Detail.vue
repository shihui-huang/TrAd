<template>
    <div style="background: #f0f0f0">
        <detail-banner :imgs="imgs" :name="name"></detail-banner>
        <detail-header></detail-header>
        <detail-infos :infos="infos"></detail-infos>
        <detail-list :commentList="commentList"></detail-list>
    </div>
</template>

<script>
import DetailBanner from './components/Banner'
import DetailHeader from './components/Header'
import DetailList from './components/List'
import DetailInfos from './components/Infos'
import axios from 'axios'
export default {
  name: 'Detail',
  components: {
    DetailBanner,
    DetailHeader,
    DetailList,
    DetailInfos
  },
  data () {
    return {
      id: '',
      name: '',
      imgs: [],
      infos: '',
      openHours: [],
      suggestedDuration: '',
      commentList: []
    }
  },
  methods: {
    getDetailInfo () {
      // = axios.get('/static/mock/detail.json?id=' + this.$route.params.id
      axios.get('/static/mock/detail.json', {
        params: {
          id: this.$route.params.id
        }
      }).then(this.handleGetDataSucc)
    },
    handleGetDataSucc (res) {
      this.id = this.$route.params.id
      res = res.data
      if (res.ret && res.data) {
        const data = res.data
        this.name = data[this.id].name
        this.imgs = data[this.id].imgs
        this.infos = data[this.id].infos
        this.commentList = data[this.id].commentList
      }
    }
  },
  activated () {
    this.getDetailInfo()
  }
}
</script>

<style lang="stylus" scoped>
</style>
