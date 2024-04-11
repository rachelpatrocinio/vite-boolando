<script>
import CardItem from './CardItem.vue';
import productData from '../assets/db.json';

export default {
    components: {
        CardItem
    },
    data(){
        return{
            products: productData.products
        }
    }
}
</script>

<template>
<main class="main-content">
    <section>
        <div class="container">
            <div class="row d-flex flex-wrap">
                <div class="col-4" v-for="(product,i) in products" :key="product.id">
                    <CardItem :item="product"/>
                </div> 
            </div>
        </div>
    </section>
</main>
</template>

<style lang="scss" scoped>
</style>