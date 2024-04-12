<script>
export default {
    props:{
        badges:{
            type: Array
        }
    }
}
</script>

<template>
    <span v-for="badge in badges" :class="badge.type === 'tag' ? 'badge__green': 'badge__red'">{{ badge.value }}</span>
</template>

<style lang="scss" scoped>
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
    order: -1;
    margin-right: 5px;
}

.badge__green{
    background-color: green;
    width: 80px;
}
</style>