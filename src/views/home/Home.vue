<template>
  <div>
    <nav-bar>
      <div slot="center">购物车</div>
    </nav-bar>
    <home-swiper :banner='banner'></home-swiper>
    <home-recommend :recommend='recommend.list'></home-recommend>
  </div>
</template>

<script>
import NavBar from 'components/common/navbar/NavBar'
import HomeSwiper from './childcomps/HomeSwiper'
import HomeRecommend from './childcomps/HomeRecommend'

import { getHomeMutltidata } from 'network/home'
export default {
  name: 'Home',
  components: {
    NavBar,
    HomeSwiper,
    HomeRecommend
  },
  data () {
    return {
      banner: [],
      recommend: []
    }
  },
  created () {
    getHomeMutltidata()
      .then(res => {
        console.log(res)
        this.banner = res.banner
        this.recommend = res.recommend
      })
  }
}
</script>

<style scoped>

</style>