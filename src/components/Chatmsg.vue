<template>
    <div class="chat-container">
        <div class="sent-msg">

        </div>
        <div class="received-msg">

        </div>
    </div>
</template>

<script>
export default {
    name: 'Chatmsg'

}
</script>

<style lang="scss">
@import "../style/common.scss";

.chat-container {
    width: 100%;
    height: 100%;
    background-image: url(../assets/img/mine.jpg);

    .sent-msg {
        background-color: $color-sent;
    }

    .received-msg {
        background-color: $color-received;
    }

}


</style>