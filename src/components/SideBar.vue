<template>
    <div class="Left-col">
    <!-- Block User -->
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
    <!-- /Block User -->

    <!-- Notifications -->
        <div class="block-notifications">
                <font-awesome-icon class="icon" icon="bell-slash" />
            <div>
                <p class="normal-text">Ricevi notifiche di nuovi messaggi</p>
                <p class="text-not-desk">Attiva notifiche desktop</p>
            </div>
        </div>
    <!-- /Notifications -->

    <!-- Search block -->
        <div class="block-search-user">
            <font-awesome-icon class="icon-search" icon="search"/>
            <input type="text" placeholder="Cerca o inizia una nuova chat" >
        </div>
    <!-- /Search block -->

    <!-- Contacts -->
        <ul class="contacts">
            <li class="single-user" v-for="(user, index) in contacts" :key="index">
                <div class="user-img">
                    <img :src="`../assets/img/avatar${user.avatar}.jpg`" :alt="user.avatar">
                </div>
                <div class="user-name">
                    {{user.name}}
                </div>
            </li>
            <div>
                <img src="../assets/img/avatar_1.jpg" alt="">
            </div>
        </ul>
    <!-- /Contacts -->

    </div>
</template>

<script>
export default {
    name: 'SideBar',
    data() {
        return {
            contacts: [
            {
                name: 'Michele',
                avatar: '_1',
                visible: true,
                messages: [
                    {
                        date: '10/01/2020 15:30:55',
                        message: 'Hai portato a spasso il cane?',
                        status: 'sent'
                    },
                    {
                        date: '10/01/2020 15:50:00',
                        message: 'Ricordati di dargli da mangiare',
                        status: 'sent'
                    },
                    {
                        date: '10/01/2020 16:15:22',
                        message: 'Tutto fatto!',
                        status: 'received'
                    }
                ],
            },
            {
                name: 'Fabio',
                avatar: '_2',
                visible: true,
                messages: [{
                    date: '20/03/2020 16:30:00',
                    message: 'Ciao come stai?',
                    status: 'sent'
                },
                    {
                        date: '20/03/2020 16:30:55',
                        message: 'Bene grazie! Stasera ci vediamo?',
                        status: 'received'
                    },
                    {
                        date: '20/03/2020 16:35:00',
                        message: 'Mi piacerebbe ma devo andare a fare la spesa.',
                        status: 'received'
                    }
                ],
            },
            {
                name: 'Samuele',
                avatar: '_3',
                visible: true,
                messages: [{
                    date: '28/03/2020 10:10:40',
                    message: 'La Marianna va in campagna',
                    status: 'received'
                },
                    {
                        date: '28/03/2020 10:20:10',
                        message: 'Sicuro di non aver sbagliato chat?',
                        status: 'sent'
                    },
                    {
                        date: '28/03/2020 16:15:22',
                        message: 'Ah scusa!',
                        status: 'received'
                    }
                ],
            },
            {
                name: 'Luisa',
                avatar: '_4',
                visible: true,
                messages: [{
                    date: '10/01/2020 15:30:55',
                    message: 'Lo sai che ha aperto una nuova pizzeria?',
                    status: 'sent'
                },
                    {
                        date: '10/01/2020 15:50:00',
                        message: 'Si, ma preferirei andare al cinema',
                        status: 'received'
                    }
                ],
            },
        ]
                }
            }

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
                    padding: 4px 0;
                    cursor: pointer;
                }
            }
            
            .block-search-user {
                display: flex;
                align-items: center;
                background-color: #fafafa;

                
                .icon-search {
                    padding: 8px;
                    font-size: 38px;
                    color: #b1b1b1;
                    background-color: #fff;
                    border: 1px solid #e9ebeb;
                    margin-left: 5px;
                    cursor: pointer;
                }
                input{
                    display: flex;
                    width: 100%;
                    flex-grow: 1;
                    margin: 5px 5px 5px 0;
                    padding: 10px;
                    border: 1px solid #e9ebeb;
                    // width: calc(100% - 5px);
                }
            }
}


</style>