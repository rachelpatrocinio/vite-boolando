<script>
import CardItem from './CardItem.vue';
import {store} from '../store.js'

export default {
    components: {
        CardItem
    },
    data(){
        return{
            store: store
        }
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