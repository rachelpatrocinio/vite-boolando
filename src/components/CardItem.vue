<script>
import CardBadges from './CardBadges.vue';
import AppModal from './AppModal.vue'
export default {
    components:{
        CardBadges,
        AppModal
    },
    props:{
        item:{
            type: Object
        }
    },
    data(){
        return{
            isOpen: false
        }
    },
    methods:{
        putInFavorites(item){
            item.isInFavorites = !item.isInFavorites
        },
        confirm(){
            this.isOpen = true
            console.log(this.isOpen)
        }
    },
    computed:{
        fiftyPercentDiscounted(){
            return (this.item.price - (this.item.price * 0.50)).toFixed(2)
        },
        thirtyPercentDiscounted(){
            return (this.item.price - (this.item.price * 0.30)).toFixed(2)
        }
    }
}
</script>

<template>
    <AppModal :open="isOpen" @close="isOpen = false" :item="item"/>
    <div class="card">
        <div class="card__header">
            <img :src="item.frontImage" alt="RELAXED FIT TEE UNISEX">
            <i  @click="putInFavorites(item)" class="wishlist-btn fa-solid fa-heart" :class="item.isInFavorites === true ? 'c-red':'c-black'"></i>
            <div class="badges d-flex">
                <CardBadges :badges="item.badges"/>
            </div>
            <div class="overlay">
                <img :src="item.backImage" alt="RELAXED FIT TEE UNISEX 2">
            </div>                
        </div>
        <div class="card__body">
            <span class="brand-name">{{ item.brand }}</span>
            <h5 @click="confirm">{{item.name}}</h5>
            <template v-for="(badge,i) in item.badges" :key="i">
                <span v-if="badge.value === '-50%'" class="price-tag c-red">{{ fiftyPercentDiscounted }}</span>
                <span v-else-if="badge.value === '-30%'" class="price-tag c-red">{{ thirtyPercentDiscounted }}</span>
            </template>
            <span class="price-tag">{{item.price}} €</span>
        </div>
    </div>
</template>

<style lang="scss" scoped>
/* CARDS */
.c-red{
    color:red;
}
.c-black{
    color:black;
}

.card__header{
    position: relative;
    img{
        display: block;
    }
}

.card__body h5{
    cursor: pointer;
}

.brand-name{
    font-size: 12px;
}

.wishlist-btn{
    cursor: pointer;
    width: 30px;
    padding: 3px;
    font-size: 12px;
    text-align: center;
    background-color: white;
    position: absolute;
    right: 0;
    top: 5px;
    z-index: 1;
}

.badges{
    position: absolute;
    bottom: 25px;
}

.price-tag{
    font-weight: 700;
    margin-right: 10px;
}

.price-tag + span {
    text-decoration: line-through;
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