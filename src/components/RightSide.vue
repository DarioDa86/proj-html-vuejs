<template>
        <header>
            <div class="actual-user">
                <div class="info-user">
                    <img class="img-users" src="../assets/img/avatar_io.jpg" alt="">
                    <div class="normal-text">
                        Nome Utente
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
    name: 'RightSide'
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