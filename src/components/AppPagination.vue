<script>

    import {store} from '../store.js';

    export default {
        name: 'AppPagination',

        data() {
            return {
                store,
            }
        }
    }
</script>

<template>

    <div class="cards-num">
        Found {{ store.cards.length }} cards
    </div>

</template>

<style lang="scss">

    .cards-num{
        padding: 26px 20px;
        background-color: #212529;
        color: white;
    }

</style>