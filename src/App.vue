<template>
  <div class="container">
    <SideBar @conversation="pastConversation" @actualUserImage ="imgUser"/>
    <div class="right-col">
      <RightSide :displayImgUser ="actualUser"/>
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
      oldMsg: [],
      actualUser: ""

    }
  },
  methods: {
    pastConversation(item) {
      this.oldMsg = item;
    },
    imgUser(elm) {
      this.actualUser = elm;
    }
  }
}
</script>

<style lang="scss">
@import "./style/common.scss";

</style>
