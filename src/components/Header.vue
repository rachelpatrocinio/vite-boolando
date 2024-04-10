<script></script>

<template>
    <header class="main-header">
        <div class="container">
            <div class="row">
                <div class="col-3">
                    <ul class="d-flex justify-start">
                        <li class="main-menu-items"><a href="#">Donna</a></li>
                        <li class="main-menu-items"><a href="#">Uomo</a></li>
                        <li class="main-menu-items"><a href="#">Bambini</a></li>
                    </ul>
                </div>
                <div class="col-3 d-flex justify-center">
                    <figure class="logo">
                        <img src="/public/boolean-logo.png" alt="Logo Boolean">
                    </figure>
                </div>
                <div class="col-3 d-flex justify-end">
                    <ul class="d-flex">
                        <li class="main-menu-links">
                            <a href="#">
                                <i class="fa-solid fa-user"></i>
                            </a>
                        </li>
                        <li class="main-menu-links">
                            <a href="#">
                                <i class="fa-solid fa-heart"></i>
                            </a>
                        </li>
                        <li class="main-menu-links">
                            <a href="#">
                                <i class="fa-solid fa-bag-shopping"></i>
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
        </div> 
    </header>

</template>

<style lang="scss" scoped>
@use '../style/partials/mixins' as *;
@use '../style/partials/variables' as *;

.main-header{
    background-color: $brand-color;
    color: white;
    box-shadow: 0 0 20px 2px rgba(0,0,0.1);
    .row{
        @include flex-between-mixin;
    }
}

.main-header .logo{
    width: 100px;
    display: $d-flex;
    align-items: center;
}

.main-header li[class^=main-menu]{
    padding: 5px;
    font-weight: 500;
}

.main-menu-items, .main-menu-links i{
    font-size: 14px;
    &:hover{
        color: black;
    }
}
</style>