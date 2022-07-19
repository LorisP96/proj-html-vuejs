<template>
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
            <div class="cart-2">
                <img src="../assets/svg/svg-9.svg" alt="">
            </div>
            <div class="circle">
                <img src="../assets/svg/svg-7.svg" alt="">
            </div>
        </div>
    </section>
</template>

<script>
export default {
    props: {
        socialIcon: Object,
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/scss/vars.scss';
@import '../assets/scss/style.scss';

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
        position: relative;

        .cart-2, .circle {
            width: 35px;
            height: 35px;
            padding: 10px;
            position: absolute;
            border-radius: 3px;
        }

        .cart-2 {
            top: 0;
            right: 0;
            background-color: $bg-white-1;
        }

        .circle {
            top: -36px;
            right: 0;
            background-color: $bg-red-1;
        }
    }
}
</style>