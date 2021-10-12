<template>
        <div class="block-user">
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
</template>

<script>
export default {
    name: 'RightSide'
}
</script>

<style lang="scss" scoped>

.block-user {
    width: 70%;
}

</style>