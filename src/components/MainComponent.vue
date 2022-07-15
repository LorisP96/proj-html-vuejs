<template>
  <main>
    <!-- INTRODUCTION -->
    <section class="intro flex">
        <div class="intro-card">
            <img src="../assets/img/h3-img-1.jpg" alt="">
        </div>
        <div class="intro-card">
            <img src="../assets/img/h3-img-2.jpg" alt="">
        </div>
        <div class="intro-card">
            <img src="../assets/img/h3-img-3.jpg" alt="">
        </div>
        <div class="intro-card">
            <img src="../assets/img/h3-img-4.jpg" alt="">
        </div>
    </section>

    <!-- HELLO -->
    <section class="hello">
        <div class="washington-review flex">
            <h3>"FORGET THE TRENDY PIZZA SHOPS, THIS HIDDEN SPOT MAKES THE BEST NEW YORK-STYLE PIZZA SLICE IN NAPLES"</h3>
            <h6>WASHINGTON POST 2018</h6>
        </div>
    </section>

    <!-- SPECIALS -->
    <section class="specials-container flex">
        <div class="special img-special">
            <img src="../assets/img/h1-img-7n.png" alt="">
        </div>
        <div class="special">
            <h2>SPECIALS*</h2>
            <span>Lorem ipsum dolor sit amet consectetur adipisicing elit. Numquam quam aliquid possimus </span>
            <ul class="special-list">
                <li class="flex">
                    <div class="price">$10</div>
                    <div class="list-product">
                        <h3>COMBO PICCOLO</h3>
                        <span>Lorem ipsum dolor sit amet consectetur adipisicing elit. Numquam quam aliquid possimus </span>
                    </div>
                </li>

                <li class="flex">
                    <div class="price">$20</div>
                    <div class="list-product">
                        <h3>COMBO MEDIO</h3>
                        <span>Lorem ipsum dolor sit amet consectetur adipisicing elit. Numquam quam aliquid possimus </span>
                    </div>
                </li>

                <li class="flex">
                    <div class="price">$30</div>
                    <div class="list-product">
                        <h3>COMBO GRANDE</h3>
                        <span>Lorem ipsum dolor sit amet consectetur adipisicing elit. Numquam quam aliquid possimus</span>
                    </div>
                </li>
            </ul>
        </div>
    </section>
  </main>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
    @import '../assets/scss/vars.scss';
    @import '../assets/scss/style.scss';
    .intro {
        padding: 6px 0;
        justify-content: space-between;

        .intro-card {
            width: calc((100% / 4) - 6px);

            img {
                width: 100%;
            }
        }
    }

    .hello {
        height: 495px;
        background-image: url(../assets/img/h3-testimonials-bckgrnd.jpg);
        background-position: center;

        .washington-review {
            justify-content: center;
            align-items: center;
            flex-direction: column;
            height: 100%;
            width: 40%;
            margin: 0 auto;
            text-align: center;
            line-height: 31px;
            
            h6 {
                color: $txt-red-1;
                font-size: 12px;
            }
        }
    }

    .specials-container {
        padding: 6px 0;
        align-items: center;

        .special {
            width: 50%;
            padding-left: 200px;
            padding-right: 310px;
            
            h2 {
                font-size: 30px;
                padding-bottom: 10px;
            }

            span {
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

                        span {
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
            }
        }
    }
</style>