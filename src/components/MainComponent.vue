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
            <div class="quot-hello"><i class="fa-solid fa-quote-left"></i></div>
            <h3>"FORGET THE TRENDY PIZZA SHOPS, THIS HIDDEN SPOT MAKES THE BEST NEW YORK-STYLE PIZZA SLICE IN NAPLES"</h3>
            <h6>WASHINGTON POST 2018</h6>
            <div class="dots flex">
                <i class="fa-solid fa-circle"></i>
                <i class="fa-solid fa-circle"></i>
                <i class="fa-solid fa-circle"></i>
            </div>
        </div>

        <div class="slice">
            <img :src="pizzaSlice" alt="pizza-hello">    
        </div>
    </section>

    <!-- SPECIALS -->
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

        <div class="slice">
            <img :src="pizzaSlice" alt="pizza-hello">    
        </div>
    </section>

    <!-- BANNER -->
    <section class="banner">
        <div class="banner-in-banner" id="top-banner"></div>
        <div class="banner-in-banner" id="mid-banner">
            <div class="slice">
                <img :src="pizzaSlice" alt="pizza-hello">    
            </div>
        </div>
        <div class="banner-in-banner" id="bot-banner"></div>
        <h2>GO AHEAD AND<br>BUILD YOUR<br>OWN PIZZA<br>WE WON'T<br>JUDGE!</h2>
    </section>

    <!-- TEAM -->
    <section class="teams flex">
        <div class="team-card">
            <img src="../assets/img/h1-team-1a-700x700.jpg" alt="team member 1">
            <div class="info-card">
                <h3>FRANK BAILEY</h3>
                <div class="job">Kitchen Porter</div>
                <div>socials</div>
            </div>
        </div>
        <div class="team-card">
            <img src="../assets/img/h1-team-2a.jpg" alt="team member 2">
            <div class="info-card">
                <h3>FRANK BAILEY</h3>
                <div class="job">Kitchen Porter</div>
                <div>socials</div>
            </div>
        </div>
        <div class="team-card">
            <img src="../assets/img/h1-team-4a.jpg" alt="team member 3">
            <div class="info-card">
                <h3>FRANK BAILEY</h3>
                <div class="job">Kitchen Porter</div>
                <div>socials</div>
            </div>
        </div>
        <div class="team-card">
            <img src="../assets/img/h1-team-3a.jpg" alt="team member 4">
            <div class="info-card">
                <h3>FRANK BAILEY</h3>
                <div class="job">Kitchen Porter</div>
                <div>socials</div>
            </div>
        </div>

        <div class="slice">
            <img :src="pizzaSlice" alt="pizza-hello">    
        </div>
    </section>

    <!-- TESTIMONIALS -->
    <section class="testimonials">
        <div class="test-cont flex">
            <div class="test-card">
                <img src="../assets/img/h1-clients-img-4.png" alt="">
                
            </div>
            <div class="test-card">
                <img src="../assets/img/h1-clients-img-3.png" alt="">
            </div>
            <div class="test-card">
                <img src="../assets/img/h1-clients-img-1.png" alt="">
            </div>
            <div class="test-card">
                <img src="../assets/img/h1-clients-img-2.png" alt="">
            </div>
            <div class="test-card">
                <img src="../assets/img/h1-clients-img-5.png" alt="">
            </div>
        </div>
    </section>

    <!-- PIZZA -->
    <section class="pizza">

        <div class="slice">
            <img :src="pizzaSlice" alt="pizza-hello">    
        </div>

        <div class="pizza-title">
            <h6>CHOOSE YOUR FLAVOR</h6>
            <h2>THE BEST PIZZA MENU IN TOWN</h2>
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ipsa in reprehenderit explicabo ipsam asperiores cumque ea consequuntur nemo porro.</p>
        </div>
        <div class="pizza-list">
            <ul class="flex">
                <li v-for="pizza, index in pizzaMenu" :key="index">
                    <img :src="pizza.img" :alt="index">
                    <h5 class="pizza-name">{{pizza.name}}</h5>
                    <h5 class="pizza-price"><span v-if="pizza.oldPrice !== ''">{{pizza.oldPrice}}</span> {{pizza.price}}</h5>
                </li>
            </ul>
        </div>
    </section>

    <!-- DEALS -->
    <section class="deals specials-container flex">
        <div class="special">
            <h6>MADE WITH LOVE</h6>
            <h2>DELISH PIZZA DEALS</h2>
            <ul class="special-list">
                <li class="flex">
                    <div class="date">
                        <div class="date-number">02</div>
                        <div class="date-month">NOV</div>
                    </div>
                    <div class="info-deals">
                        <h3>TRADITIONAL NEAPOLITAN PIES IN KYOTO PIZZA MERCATO</h3>
                        <h6>204 E. Pizzetta Tommaso</h6>
                    </div>
                </li>

                <li class="flex">
                    <div class="date">
                        <div class="date-number">03</div>
                        <div class="date-month">NOV</div>
                    </div>
                    <div class="info-deals">
                        <h3>TERRAZZA PATIO DINING SPACE OPENING THIS WEEKEND</h3>
                        <h6>204 E. Pizzetta Tommaso</h6>
                    </div>
                </li>

                <li class="flex">
                    <div class="date">
                        <div class="date-number">05</div>
                        <div class="date-month">NOV</div>
                    </div>
                    <div class="info-deals">
                        <h3>SIENNA PRIVATE DINING ROOM WITH STEPHAN BRUNN</h3>
                        <h6>204 E. Pizzetta Tommaso</h6>
                    </div>
                </li>
            </ul>
        </div>
        <div class="special">
            <img src="../assets/img/h3-img-5a.jpg" alt="">
        </div>
    </section>

    
  </main>
</template>

<script>
export default {
    props: {
        pizzaMenu: Array,
        pizzaSlice: String,
    }
}
</script>

<style lang="scss" scoped>
    @import '../assets/scss/vars.scss';
    @import '../assets/scss/style.scss';
    // INTRO
    .intro {
        padding: 8px 0;
        justify-content: space-between;

        .intro-card {
            width: calc((100% / 4) - 8px);
        }
    }

    // HELLO
    .hello {
        height: 495px;
        background-image: url(../assets/img/h3-testimonials-bckgrnd.jpg);
        background-position: -100px ;
        position: relative;

        .slice {
            top: 85%;
        }

        .washington-review {
            justify-content: center;
            align-items: center;
            flex-direction: column;
            height: 100%;
            width: 40%;
            margin: 0 auto;
            text-align: center;
            line-height: 31px;

            .quot-hello {
                font-size: 75px;
                color: $txt-gold-1;
                padding-bottom: 15px;
            }

            .dots {
                color: $txt-white-2;
                padding-top: 25px;
                font-size: 7px;
                align-items: center;
                
                i {
                    padding-inline: 3px;

                    &:first-child {
                        font-size: 9px;
                        color: $txt-gold-1;
                    }
                }
            }
        }
    }

    // SPECIALS
    .specials-container {
        padding: 8px 0;
        align-items: center;
        position: relative;

        .slice {
            top: 80%;
        }

        .special {
            width: 50%;
            padding-left: 200px;
            padding-right: 310px;
            
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

    // BANNER
    .banner {
        position: relative;
        height: 550px;
        .banner-in-banner {
            background-image: url(../assets/img/h3-background-img.jpg);
            background-repeat: repeat;
            background-size: 1600px;
            height: 25%;
        }

        #top-banner {
            background-position: bottom;
        }

        #mid-banner {
            background-position: top;
            height: 50%;
            position: relative;

            .slice {
                top: 80%;
            }
        }

        #bot-banner {
            background-position: center;
        }

        h2 {
            position: absolute;
            top: 50%;
            left: 40%;
            transform: translate(-50%, -50%);
            width: 500px;
            color: $txt-white-1;
            font-size: 55px;
            line-height: 60px;
        }
    }

    // TEAM
    .teams {
        padding-block: 8px;
        position: relative;

        .team-card {
            width: calc(100% / 4);

            .info-card {
                width: 100%;
                height: 100%;
                background-color: $bg-red-3;
                display: none;
                border: 25px solid $border-white-1;
                flex-direction: column;
                justify-content: center;
                align-items: center;
                color: $txt-white-1;

                h3 {
                    font-size: 25px;
                    font-weight: 400;
                }

                .job {
                    font-size: 15px;
                    font-weight: 300;
                    padding-bottom: 15px;
                }
            }

            &:hover img {
                display: none;
            }

            &:hover div {
                display: flex;
            }
        }

        .slice{
            top: 80%;
        }
    }

    // TESTIMONIALS
    .testimonials {
        background-color: $bg-white-3;

        .test-cont {
            width: 60%;
            margin: 0 auto;
            align-items: center;
            padding-block: 90px;

            .test-card {
                width: calc(100% / 5);
            }
        }
    }

    // PIZZA
    .pizza {
        padding-top: 100px;
        padding-bottom: 150px;
        position: relative;

        .slice {
            top: 28%;
        }

        .pizza-title {
            padding-bottom: 70px;
            width: 40%;
            margin: 0 auto;
            text-align: center;

            h2 {
                padding-bottom: 10px;
                font-size: 30px;
                color: $txt-black-3;
            }

            p {
                color: $txt-grey-6;
                font-size: 15px;
            }
        }
        .pizza-list {
        
            ul {
                // nel caso in cui si volessero vedere impostare 
                // overflow-x auto, impostare justify content baseline e scommentare la scrollbar
                overflow-x: hidden;
                justify-content: center;

                // &::-webkit-scrollbar {
                //     background-color: #434343;
                //     width: 16px;
                //     height: 8px;
                // }

                // &::-webkit-scrollbar-track {
                //     background-color:#2e2e2e81;
                // }

                // &::-webkit-scrollbar-thumb {
                //     background-color: #a4a4a4;
                //     border-radius: 16px;
                // }

                // &::-webkit-scrollbar-button {
                //     display:none;
                // }

                li {
                    width: calc(100% / 5.2);
                    text-align: center;
                    flex-shrink: 0;
                    

                    &:nth-child(3) {
                        position: relative;

                        &::before {
                            content: url(../assets/svg/svg-5.svg);
                            width: 50px;
                            position: absolute;
                            top: 15px;
                            right: 80px;
                            filter: invert(30%) sepia(55%) saturate(1897%) hue-rotate(344deg) brightness(96%) contrast(99%);
                        }

                        &::after {
                            content: "SOLD";
                            color: $txt-white-1;
                            position: absolute;
                            top: 30px;
                            right: 90px;
                            z-index: 1;
                            font-size: 12px;
                        }
                    }

                    img {
                        width: 60%;
                        margin: 0 auto;
                        display: block;
                    }

                    .pizza-name, .pizza-price {
                        font-size: 15px;
                    }
                    .pizza-name {
                        padding-top: 15px;
                        color: $txt-gold-1;
                    }

                    .pizza-price {
                        color: $txt-red-1;
                        padding-top: 3px;

                        span {
                            color: $txt-white-2;
                            text-decoration: line-through;
                        }
                    }
                }
            }
        }
        
    }

    // DEALS
    .deals {
        align-items: flex-start;
        padding-bottom: 0;

        h6 {
            font-weight: 400;
            font-size: 10px;
        }
        .special:first-child {
            background-color: $bg-black-1;
            color: $txt-white-1;
            padding-block: 110px;

            .special-list {
                li {
                    padding-block: 40px;
                    border-bottom: 1px dotted $border-gold;

                    .date {
                        text-align: center;
                        padding-right: 35px;

                        .date-number {
                            font-size: 40px;
                            font-weight: bolder;
                            color: $txt-red-2;
                            padding-top: 0;
                            line-height: 40px;
                            -webkit-text-stroke: 1px $txt-red-2;
                        }
                    }

                    &:last-child {
                            padding-bottom: 0;
                        }

                    h3 {
                        font-weight: 500;
                        font-size: 20px;
                    }

                    h6 {
                        padding-top: 8px;
                        font-weight: 300;
                    }

                    &:last-child {
                        border-bottom: none;
                    }

                    .info-deals {
                        h6 {
                            &::before {
                                font-family: "Font Awesome 5 Free";
                                content: "\f3c5";
                                display: inline-block;
                                padding-right: 10px;
                                font-weight: 900;
                                font-size: 12px;
                            }
                        }
                    }
                }
            }
        }
        .special:last-child {
            padding: 0;
        }
    }
</style>