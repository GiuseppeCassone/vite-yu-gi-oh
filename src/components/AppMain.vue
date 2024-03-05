<script>
    import axios from 'axios';

    import AppPagination from './AppPagination.vue';
    import CardItem from './CardItem.vue';

    import {store} from '../store.js';


    export default {
        name: "AppMain",

        components: {
            AppPagination,
            CardItem,
        },

        data() {
            return {
                store,
            }
        },

        methods: {

            searchArchetype() {
                axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php').then(res => {
                    console.log(res.data);
                    this.store.archetype = res.data;
                })
            }
        },

        created() {
            this.searchArchetype()
        }



        
    }
</script>

<template>
    <div class="container">
        
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