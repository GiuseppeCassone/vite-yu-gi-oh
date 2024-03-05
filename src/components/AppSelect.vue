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
    <div id="card-archetype">
        <select class="btn btn-light" @change="$emit('search')" v-model="store.selectSearch">
            <option value="">Scegli Archetipo</option>
            <option :value="currentArchetype.archetype_name" v-for="(currentArchetype, index) in store.archetype">{{ currentArchetype.archetype_name }}</option>
        </select>           
    </div>

</template>

<style lang="scss">
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

</style>