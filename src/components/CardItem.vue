<script>

    export default {
        name: 'CardItem',

        props: {
            card: Object,
        },
    }
</script>

<template>
    
    <div class="card">
        <img :src="card.card_images[0].image_url" :alt="card.name">
        <h3>{{ card.name }}</h3>
        <span>{{ card.archetype }}</span>
    </div>

</template>

<style lang="scss">

    .card{
        display: flex;
        flex-direction: column;

        width: calc(100% / 5 - 40px / 5 * 4);
        text-align: center;
        background-color: #D48F38;

        h3{
            color: white;
            padding: 25px 0;
        }
    }

</style>