<script>

    import AppPagination from './AppPagination.vue';
    import CardItem from './CardItem.vue';

    import {store} from '../store.js';


    export default {
        name: "AppMain",

        components: {
            AppPagination,
            CardItem
        },

        data() {
            return {
                store,
            }
        }

        
    }
</script>

<template>
    <div class="container">
        <div id="card-archetype">
            <select class="btn btn-light">
                <option value="Alien">Alien</option>
                <option value="Noble Knight">Noble Knight</option>
                <option value="Infernoble Arms">Infernoble Arms</option>
            </select>
        </div>
        
        <div class="card-container">
            <AppPagination></AppPagination>

            <div class="cards-inner">
                <CardItem v-for="currentCard in store.cards" :card="currentCard"></CardItem>
            </div>
            
        </div>

    </div>
</template>

<style lang="scss">
@use '../styles/variables' as *;

    .container{
        max-width: 1200px;
        margin-left: auto;
        margin-right: auto;
        padding: 34px 0 0;

        #card-archetype {
            width: 20%;
            padding-left: 10px;
            margin-bottom: 34px;


            .btn{
                padding: 12px 10px;
                border-radius: 12px;
                
                background-color: white;
            }
        }

        .card-container {
            width: 100%;
            padding: 72px 72px 10px 72px;
            background-color: white;

            .cards-inner{
                display: flex;
                flex-wrap: wrap;
                row-gap: 25px;
                column-gap: $cardGap;
            }
        }

    }

</style>