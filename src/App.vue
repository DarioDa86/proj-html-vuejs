<template>
  <div class="container">
    <SideBar @conversation="pastConversation"/>
    <div class="right-col">
      <RightSide/>
      <Chatmsg :displayMsg ="oldMsg"/>
      <ChatText/>
    </div>
  </div>
</template>

<script>
import SideBar from './components/SideBar.vue'
import RightSide from './components/RightSide.vue'
import Chatmsg from './components/Chatmsg.vue'
import ChatText from './components/ChatText.vue'

export default {
  name: 'App',
  components: {
    SideBar,
    RightSide,
    Chatmsg,
    ChatText
  },
  data() {
    return {
      oldMsg: []
    }
  },
  methods: {
    pastConversation(item) {
      this.oldMsg = item;
    }
  }
}
</script>

<style lang="scss">
@import "./style/common.scss";

</style>
