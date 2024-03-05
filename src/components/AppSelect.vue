<script>

import {store} from '../store.js';

    export default {
        name: 'AppSelect',

        data() {
            return {
                store,
            }
        }
    }

</script>

<template>

    <select class="btn btn-light" @click="$emit('search')">
        <option value="">Scegli Archetipo</option>
        <option value="Archetype" v-for="(currentArchetype, index) in store.archetype">{{ currentArchetype.archetype_name }}</option>
    </select>

</template>

<style lang="scss">

    .btn{
        padding: 12px 10px;
        border-radius: 12px;
        background-color: white;
    }

</style>