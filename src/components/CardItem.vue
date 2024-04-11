<script>
export default {
    props:{
        item:{
            type: Object
        }
    }
}
</script>

<template>
    <div class="card">
        <div class="card__header">
            <img :src="item.frontImage" alt="RELAXED FIT TEE UNISEX">
            <span class="wishlist-btn"> &hearts;</span>
            <div class="badges">
                <!-- <span class="badge__red"></span> -->
                <!-- <span class="badge__green"></span> -->
            </div>
            <div class="overlay">
                <img :src="item.backImage" alt="RELAXED FIT TEE UNISEX 2">
            </div>                
        </div>
        <div class="card__body">
            <span class="brand-name">{{ item.brand }}</span>
            <h5>{{item.name}}</h5>
            <span class="price-tag">{{item.price}} €</span>
            <span class="price-tag-line-through"></span>
        </div>
    </div>
</template>

<style lang="scss" scoped>
/* CARDS */

.card__header{
    position: relative;
    img{
        display: block;
    }
}

.brand-name{
    font-size: 12px;
}

.wishlist-btn{
    width: 30px;
    padding: 3px;
    font-size: 12px;
    text-align: center;
    background-color: white;
    position: absolute;
    right: 0;
    top: 5px;
    z-index: 100;
    &:hover{
        color: red;
        cursor: pointer;
    }
}

.badges{
    position: absolute;
    bottom: 25px;
}

span[class^=badge]{
    color: white;
    padding: 3px;
    font-size: 10px;
    font-weight: 700;
    text-align: center;
    display: inline-block;
    z-index: 100;
}
.badge__red{
    background-color: red;
    width: 50px;
}

.badge__green{
    background-color: green;
    width: 80px;
}

.price-tag{
    color: red;
    font-weight: 700;
}

.price-tag-line-through{
    text-decoration: line-through;
}

.overlay{
    position: absolute;
    top: 0;
    bottom: 0;
    opacity: 0;
}

.card__header:hover .overlay{
    opacity: 1;
    transition: 500ms ease-in-out;
}

.card__header:hover .badges{
    z-index: 100;
}</style>