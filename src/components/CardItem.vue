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
        <h2>{{ card.name }}</h2>
        <span>{{ card.archetype }}</span>
    </div>

</template>

<style lang="scss">

</style>