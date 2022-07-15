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

    <!-- BANNER -->
    <section class="banner">
        <div class="banner-in-banner" id="top-banner"></div>
        <div class="banner-in-banner" id="mid-banner"></div>
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
            <img src="../assets/img/h1-team-3a.jpg" alt="team member 3">
            <div class="info-card">
                <h3>FRANK BAILEY</h3>
                <div class="job">Kitchen Porter</div>
                <div>socials</div>
            </div>
        </div>
        <div class="team-card">
            <img src="../assets/img/h1-team-4a.jpg" alt="team member 4">
            <div class="info-card">
                <h3>FRANK BAILEY</h3>
                <div class="job">Kitchen Porter</div>
                <div>socials</div>
            </div>
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
    // INTRO
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

    // HELLO
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

    // SPECIALS
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

    // TESTIMONIALS
    .teams {
        padding-block: 6px;

        .team-card {
            width: calc(100% / 4);

            img {
                width: 100%;
            }

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
    }
</style>