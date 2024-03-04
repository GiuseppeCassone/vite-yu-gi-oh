<script>
  import axios from 'axios';

  import { store } from './store.js';

  import AppNav from './components/AppNav.vue';
  import AppMain from './components/AppMain.vue';
  import AppLoader from './components/AppLoader.vue';


  export default {

    data() {

      return {
          loading: true,
          store,
      }
    },

    created() {

      axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0').then(res => {
        console.log(res.data.data),
          this.store.cards = res.data.data;
          this.loading = false;
      })
    },
      
    components: {
      AppNav,
      AppMain,
      AppLoader,
    },
  }

</script>

<template>
  <AppLoader v-if="loading"></AppLoader>
  <AppNav></AppNav>
  <AppMain></AppMain>
</template>

<style lang="scss">

</style>
