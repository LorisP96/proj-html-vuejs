<template>
    <section class="pizza">

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
</template>

<script>
export default {
    props: {
        pizzaMenu: Array,
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/scss/vars.scss';
@import '../assets/scss/style.scss';

.pizza {
    padding-block: 100px;

    .pizza-title {
        padding-bottom: 100px;
        width: 30%;
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
            overflow-x: auto;
            padding-bottom: 50px;
            // justify-content: center;

            &::-webkit-scrollbar {
                background-color: #434343;
                width: 16px;
                height: 8px;
            }

            &::-webkit-scrollbar-track {
                background-color:#2e2e2e81;
            }

            &::-webkit-scrollbar-thumb {
                background-color: #a4a4a4;
                border-radius: 16px;
            }

            &::-webkit-scrollbar-button {
                display:none;
            }

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
</style>