<template>
    <section class="specials-container flex">
        <div class="special img-special">
            <img src="../assets/img/h1-img-7n.png" alt="">
        </div>
        <div class="special">
            <h2>SPECIALS*</h2>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Numquam quam aliquid possimus </p>
            <ul class="special-list">
                <li class="flex">
                    <div class="price">$10</div>
                    <div class="list-product">
                        <h3>COMBO PICCOLO</h3>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Numquam quam aliquid possimus </p>
                    </div>
                </li>

                <li class="flex">
                    <div class="price">$20</div>
                    <div class="list-product">
                        <h3>COMBO MEDIO</h3>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Numquam quam aliquid possimus </p>
                    </div>
                </li>

                <li class="flex">
                    <div class="price">$30</div>
                    <div class="list-product">
                        <h3>COMBO GRANDE</h3>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Numquam quam aliquid possimus</p>
                    </div>
                </li>
            </ul>
        </div>
    </section>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
@import '../assets/scss/vars.scss';
@import '../assets/scss/style.scss';

.specials-container {
    padding: 8px 0;
    align-items: center;

    .special {
        // style.scss
        
        h2 {
            font-size: 30px;
            padding-bottom: 10px;
        }

        p {
            color: $txt-grey-6;
            display: inline-block;
            padding-bottom: 15px;
            font-size: 15px;
        }

        .special-list {
            li {
                padding-block: 15px;
                .price {
                    font-size: 22px;
                    font-weight: bold;
                    padding-right: 30px;
                    color: $txt-red-2;
                }

                .list-product {

                    h3 {
                        font-size: 22px;
                        font-weight: bold;
                    }

                    p {
                        display: inline-block;
                        padding-top: 8px;
                        padding-bottom: 0;
                        font-size: 13px;
                    }
                }   
            }
        }
    }
    .img-special {
        background-image: url(../assets/img/h1-img-4.jpg);
        background-position: center;
        text-align: center;
        background-size: cover;
        padding-block: 150px ;
        padding-right: 0;
        padding-left: 0;
        img {
            width: 38%;
            margin: 0 auto;
        }
    }
}
</style>