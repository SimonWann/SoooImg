<template>
  <div id="app">
    <scale></scale>
    <div id="content">
      <side-bar></side-bar>
      <img-area></img-area>
    </div>
  </div>
</template>
<script>
import imgArea from './components/imgArea'
import scale from './components/scale'
import sideBar from './components/sidebar'

export default {
  components: {
    imgArea,
    scale,
    sideBar
  }
}
</script>
<style lang="less">
  #content{
  
  }
</style>
