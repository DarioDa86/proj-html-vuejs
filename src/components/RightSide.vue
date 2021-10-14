<template>
        <header>
            <div class="actual-user">
                <div class="info-user">
                    <img class="img-users" :src="require(`../assets/img/avatar${currentUser.avatar}.jpg`)" alt="prova">
                    <div class="normal-text">
                        {{currentUser.name}}
                </div>
                </div>
                <div class="icons">
                    <font-awesome-icon class="icon" icon="search" />
                    <font-awesome-icon class="icon" icon="paperclip" />
                    <font-awesome-icon class="icon" icon="ellipsis-v" />
                </div>
            </div>
        </header>
</template>

<script>
export default {
    name: 'RightSide',
    props: ['displayImgUser'],
    data() {
        return {
            currentUser: {
                avatar:"",
                name: ""
            }
        }
    },
    created() {
        this.setBaseAvatar()
    
    },
    watch: {
        displayImgUser() {
            this.currentUser= {
                avatar:this.displayImgUser.avatar,
                name:this.displayImgUser.name,
            };
        }
    },
    methods: {
        setBaseAvatar: function() {
            this.currentUser = {
                name:"Michele",
                avatar:"_1"
            }
            console.log("provaGianluca")
        }
    }

}
</script>

<style lang="scss">
@import "../style/common.scss";

header {


    .actual-user, .info-user {
        background-color: $bg-grey;
        display: flex;
        justify-content: space-between;
        align-items: center;

        .icons {
            color: $color-icons;
            display: inline-block;
            font-size: 20px;
            margin-right: 10px;
            
            .icon {
                margin-right: 10px;
                cursor: pointer;
            }
        }
    }
}

</style>