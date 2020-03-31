<template>
  <div id="app">
    <MainHeader></MainHeader>
    <Tabbar></Tabbar>
    <keep-alive include="Singer,Search">
      <router-view></router-view>
    </keep-alive>
  </div>
</template>

<script>
import Vue from 'vue'
import MainHeader from './components/MainHeader'
import Tabbar from './components/Tabbar'
import VueLazyload from 'vue-lazyload'
Vue.use(VueLazyload, {
  // 可以通过配置loading来设置图片还未加载好之前的占位图片
  loading: require('./assets/images/loading.png')
})
export default {
  name: 'App',
  components: {
    MainHeader,
    Tabbar
  }
}
</script>

<style lang="scss">

</style>
