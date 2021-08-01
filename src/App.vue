<template>
  <div id="app">
    <router-view />
    <MainTarBar></MainTarBar>
  </div>
</template>

<script>
import MainTarBar from 'components/content/tarbar/MainTarBar'

export default {
  name: 'App',
  components: {
    MainTarBar
  }
}
</script>

<style>
@import url(assets/css/common/base.css);
</style>


