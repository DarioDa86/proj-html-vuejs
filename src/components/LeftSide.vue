<template>
    <div class="Left-col">
        <div class="block-user">
            <div class="info-user">
                <img class="img-users" src="../assets/img/avatar_io.jpg" alt="">
                <div class="normal-text">
                    Nome Utente
                </div>
            </div>
            <div class="icons">
                <font-awesome-icon class="icon" icon="circle-notch" />
                <font-awesome-icon class="icon" icon="comment-alt" />
                <font-awesome-icon class="icon" icon="ellipsis-v" />
            </div>
        </div>
        <div class="block-notifications">
                <font-awesome-icon class="icon" icon="bell-slash" />
            <div>
                <p class="normal-text">Ricevi notifiche di nuovi messaggi</p>
                <p class="text-not-desk">Attiva notifiche desktop</p>
            </div>
        </div>
        <div class="block-search-user">
                        <div class="lens-btn">
                            <i class="fas fa-search"></i>
                        </div>
                        <div class="search-user">
                            <input type="text" placeholder="Cerca o inizia una nuova chat" >
                        </div>
                    </div>
    </div>
</template>

<script>
export default {
    name: 'LeftSide'

}
</script>

<style lang="scss">


.Left-col {
    width: 30%;
    
    .block-user {
        border-right: 1px solid #b1b1b1;
    }

    .block-notifications {
        background-color: #8edafc;
        display: flex;
        align-items: center;

        .icon{
            color: #8edafc;
            background-color: #f2fbff;
            font-size: 35px;
            border-radius: 50%;
            margin: 15px 5px 15px 15px;
            padding: 3px;
            cursor: pointer;
        }
    }
    

}


</style>