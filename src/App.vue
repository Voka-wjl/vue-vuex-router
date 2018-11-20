<template>
  <div id="app">
    <div class="nav">
      <li><router-link to="/Home">Home</router-link></li>
      <li><router-link to="/Cart">Cart</router-link></li>
    </div>
    <div class="app-con">
        <router-view></router-view>
    </div>

  </div>
</template>
<style lang="scss" scoped>
  @import './assets/common.scss';
</style>
<script>
import './assets/rem.js'
export default {
  name: 'App'
}
</script>


