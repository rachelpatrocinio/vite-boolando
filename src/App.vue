<script>
  import AppHeader from './components/AppHeader.vue';
  import AppMain from './components/AppMain.vue';
  import AppFooter from './components/AppFooter.vue';
  import axios from 'axios';
  import {store} from './store.js';

  export default {
    components: {
      AppHeader,
      AppMain,
      AppFooter
    },
    data(){
        return{
            store: store,
        }
    },
    methods: {
      fetchProducts(){
        axios
            .get("http://localhost:3000/products")
            .then((response) => {
                store.products = response.data
          })
      }
    },
    created(){
      this.fetchProducts()
    }
  }

</script>

<template>
  <AppHeader/>
  <AppMain/>
  <AppFooter/>
</template>

<style lang="scss">
  @use './style/general';
</style>
