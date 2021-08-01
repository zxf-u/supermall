<template>
  <div>
    <tar-bar>
      <tar-bar-item path='/home'>
        <img slot="slot-icon" src="~assets/img/tarbar/home.svg" alt="">
        <img slot="slot-icon-active" src="~assets/img/tarbar/home_active.svg" alt="">
        <div slot="slot-text">首页</div>
      </tar-bar-item>
      <tar-bar-item path='/category'>
        <img slot="slot-icon" src="~assets/img/tarbar/category.svg" alt="">
        <img slot="slot-icon-active" src="~assets/img/tarbar/home_active.svg" alt="">
        <div slot="slot-text">分类</div>
      </tar-bar-item>
      <tar-bar-item path='/cart'>
        <img slot="slot-icon" src="~assets/img/tarbar/shopcart.svg" alt="">
        <img slot="slot-icon-active" src="~assets/img/tarbar/home_active.svg" alt="">
        <div slot="slot-text">购物车</div>
      </tar-bar-item>
      <tar-bar-item path='/profile'>
        <img slot="slot-icon" src="~assets/img/tarbar/profile.svg" alt="">
        <img slot="slot-icon-active" src="~assets/img/tarbar/home_active.svg" alt="">
        <div slot="slot-text">我的</div>
      </tar-bar-item>
    </tar-bar>
  </div>
</template>

<script>
import TarBar from 'components/common/tarbar/TarBar'
import TarBarItem from 'components/common/tarbar/TarBarItem'
export default {
  name: 'MainTarBar',
  components: {
    TarBar,
    TarBarItem
  }
}
</script>

<style scoped>

</style>