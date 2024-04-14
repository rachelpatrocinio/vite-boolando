<script>
import CardItem from './CardItem.vue';
import {store} from '../store.js';
import axios from 'axios';

export default {
    components: {
        CardItem
    },
    data(){
        return{
            store: store,
            products: store.products
        }
    },
    mounted(){
        axios
            .get("http://localhost:3000/products")
            .then((response) => {
                for(let i = 0; i < response.data.length; i++){
                    const result = response.data[i]
                    this.products.push(result)
                }
            })
     }

}
</script>

<template>
<main class="main-content">
    <section>
        <div class="container">
            <div class="row d-flex flex-wrap">
                <div class="col-4" v-for="(product,i) in this.store.products" :key="product.id">
                    <CardItem :item="product"/>
                </div> 
            </div>
        </div>
    </section>
</main>
</template>

<style lang="scss" scoped>
</style>