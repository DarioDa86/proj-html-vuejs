<template>
    <div class="chat-text-container">
        <font-awesome-icon class="icon" icon="smile" />
        <input type="text" placeholder="Scrivi un messaggio" @keyup.enter="sendMsg()">
        <font-awesome-icon class="icon" icon="microphone" />
    </div>
</template>

<script>
export default {
    name: 'ChatText',

    methods: {

        sendMsg() {
            this.contacts[this.indexCurrentContact].messages.push({
				
				message: this.newMessage,
				status: 'sent'
			});
			
			this.newMessage = "";

			setTimeout(() => {
				this.contacts[this.indexCurrentContact].messages.push({
					
					message: 'ok',
					status: 'recived'
				});
			}, 1000);
		},
        
    }

}
</script>

<style lang="scss">
@import "../style/common.scss";


.chat-text-container {
    width: 100%;
    height: 70px;
    background-color: $bg-grey;
    display: flex;
    justify-content: space-between;
    align-items: center;

    .icon {
        color: $color-icons;
        font-size: 25px;
        margin: 0 20px;
        cursor: pointer;
    }
    input {
        border: none;
        border-radius: 5px;
        display: flex;
        width: 100%;
        margin: 5px 5px 5px 0;
        padding: 10px;
    }

}

</style>