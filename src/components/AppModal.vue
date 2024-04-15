<script>
export default {
    props:{
        open: {
            type: Boolean,
            default: false
        },
        item: {
            type: Object
        }
    }
}
</script>

<template>
    <div v-if="open === true" class="modal-container">
        <div class="modal-row d-flex">
            <span class="close" @click="$emit('close')">X</span>
            <div class="col-6">
                <img :src="item.frontImage" alt="">
                <img :src="item.backImage" alt="">
            </div>
            <div class="col-6">
                <h2 class="mb-10">{{ item.name }}</h2>
                <hr>
                <h5 class="mt-10">{{ item.brand }}</h5>
                <h5 class="mt-10">{{ item.price }} €</h5>
                
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../style/general';

.modal-container{
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: rgba($color: black, $alpha: 0.8);
    display: flex;
    align-items: center;
    z-index: 100;
    height: 100vh;

    .modal-row{
        width: 50%;
        margin: 0 auto;
        background-color: white;
        position: relative;
        padding: 20px;
        height: 60%;
        overflow: auto;

        .close{
        position: absolute;
        top:10px;
        right: 10px;
        cursor: pointer;
        }
    }
}
</style>