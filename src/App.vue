<template>
  <div class="container">
    <LeftSide/>
    <RightSide/>
  </div>
</template>

<script>
import LeftSide from './components/LeftSide.vue'
import RightSide from './components/RightSide.vue'

export default {
  name: 'App',
  components: {
    LeftSide,
    RightSide
  }
}
</script>

<style lang="scss">
@import "./style/common.scss";

</style>
