<script></script>

<template>
<main class="main-content">
    <section>
        <div class="container">
            <div class="row d-flex flex-wrap">
                <div class="col-4">
                    <div class="card">
                        <div class="card__header">
                            <img src="/public/1.webp" alt="RELAXED FIT TEE UNISEX">
                            <span class="wishlist-btn"> &hearts;</span>
                            <div class="badges">
                                <span class="badge__red">-50%</span>
                                <span class="badge__green">Sostenibilità</span>
                            </div>
                            <div class="overlay">
                                <img src="/public/1b.webp" alt="RELAXED FIT TEE UNISEX 2">
                            </div>                
                        </div>
                        <div class="card__body">
                            <span class="brand-name">Levi's</span>
                            <h5>RELAXED FIT TEE UNISEX</h5>
                            <span class="price-tag">14,99 €</span>
                            <span class="price-tag-line-through">29,99 €</span>
                        </div>
                    </div>
                </div> 
                <div class="col-4">
                    <div class="card">
                        <div class="card__header">
                            <img src="/public/2.webp" alt="ROSES TEE">
                            <span class="wishlist-btn"> &hearts;</span>
                            <div class="badges">
                                <span class="badge__red">-30%</span>
                            </div>
                            <div class="overlay">
                                <img src="/public/2b.webp" alt="RELAXED FIT TEE UNISEX 2">
                            </div> 
                        </div>
                        <div class="card__body">
                            <span class="brand-name">Guess</span>
                            <h5>ROSES TEE</h5>
                            <span class="price-tag">20,99 €</span>
                            <span class="price-tag-line-through">29,99 €</span>
                        </div>
                    </div>
                </div>
                <div class="col-4">
                    <div class="card">
                        <div class="card__header">
                            <img src="/public/3.webp" alt="VOGLIA DI COLORI PASTELLO">
                            <span class="wishlist-btn"> &hearts;</span>
                            <div class="badges">
                                <span class="badge__red">-30%</span>
                            </div>
                            <div class="overlay">
                                <img src="/public/3b.webp" alt="RELAXED FIT TEE UNISEX 2">
                            </div>  
                        </div>
                        <div class="card__body">
                            <span class="brand-name">Come Zucchero Filato</span>
                            <h5>VOGLIA DI COLORI PASTELLO</h5>
                            <span class="price-tag">129,99 €</span>
                            <span class="price-tag-line-through">184,99 €</span>

                        </div>
                    </div>
                </div>
                <div class="col-4">
                    <div class="card">
                        <div class="card__header">
                            <img src="/public/4.webp" alt="TEE UNISEX">
                            <span class="wishlist-btn"> &hearts;</span>
                            <div class="badges">
                                <span class="badge__red">-50%</span>
                                <span class="badge__green">Sostenibilità</span>
                            </div>
                            <div class="overlay">
                                <img src="/public/4b.webp" alt="RELAXED FIT TEE UNISEX 2">
                            </div> 
                        </div>
                        <div class="card__body">
                            <span class="brand-name">Levi's</span>
                            <h5>TEE UNISEX</h5>
                            <span class="price-tag">14,99 €</span>
                            <span class="price-tag-line-through">29,99 €</span>
                        </div>
                    </div>
                </div>
                <div class="col-4">
                    <div class="card">
                        <div class="card__header">
                            <img src="/public/5.webp" alt="STRIPE BODICE">
                            <span class="wishlist-btn"> &hearts;</span>
                            <div class="overlay">
                                <img src="/public/5b.webp" alt="RELAXED FIT TEE UNISEX 2">
                            </div> 
                        </div>
                        <div class="card__body">
                            <span class="brand-name">Maya Deluxe</span>
                            <h5>STRIPE BODICE</h5>
                            <span class="price-tag">99,99 €</span>
                        </div>
                    </div>
                </div>
                <div class="col-4">
                    <div class="card">
                        <div class="card__header">
                            <img src="/public/6.webp" alt="MAGLIONE - BLACK">
                            <span class="wishlist-btn"> &hearts;</span>
                            <div class="badges">
                                <span class="badge__green">Sostenibilità</span>
                            </div> 
                            <div class="overlay">
                                <img src="/public/6b.webp" alt="RELAXED FIT TEE UNISEX 2">
                            </div> 
                        </div>
                        <div class="card__body">
                            <span class="brand-name">Esprit</span>
                            <h5>MAGLIONE - BLACK</h5>
                            <span class="price-tag">29,99 €</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</main>
</template>

<style>
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
}
</style>