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
        <div class="modal-row">
            <span class="close" @click="$emit('close')">X</span>
            <div class="col">
                <img src="" alt="">
            </div>
            <div class="col">
                <h2></h2>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.modal-container{
    position: absolute;
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

        .close{
        position: absolute;
        top:10px;
        right: 10px;
        cursor: pointer;
        }
    }
}
</style>