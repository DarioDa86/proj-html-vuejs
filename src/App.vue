<template>
  <div class="container">
    <SideBar/>
    <RightSide/>
  </div>
</template>

<script>
import SideBar from './components/SideBar.vue'
import RightSide from './components/RightSide.vue'

export default {
  name: 'App',
  components: {
    SideBar,
    RightSide
  }
}
</script>

<style lang="scss">
@import "./style/common.scss";

</style>
