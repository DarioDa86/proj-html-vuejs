<template>
    <div class="chat-container">

        <ul>
            <li :class="[message.status == 'sent' ? 'msg sent-msg' : 'msg']" v-for="(message, index) in displayMsg" :key="index">
                {{message.message}}
                <div class="date-hour" >{{message.date}}</div>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'Chatmsg',
    props: ['displayMsg']
}
</script>

<style lang="scss">
@import "../style/common.scss";

.chat-container {
    width: 100%;
    height: calc(100% - 140px);
    padding: 20px 20px;
    background-image: url(../assets/img/mine.jpg);
    overflow-y: scroll;
    display: flex;
    flex-direction: column;

    .msg {
        background-color: $color-received;
        border-radius: 10px;
        padding: 10px;
        max-width: 45%;
        list-style: none;
        margin-top: 10px;
    }

    .sent-msg {
        background-color: $color-sent;
        margin-left: auto;
    }

    .date-hour {
        font-size: 12px;
        color: grey;
        margin-top: 3px;
    }

}


</style>