<template>
  <header>
    <nav class="flex">
        <div class="btn">
            <button>ORDER ONLNE</button>
        </div>
        <div class="list flex">
            <ul class="home">
                <li v-for="element, index in navBeforeImg" :key="'a' + index" >{{ element }}</li>
            </ul>
            <div class="logo">
                <img src="../assets/img/h5-logo-divided-header.png" alt="logo">
            </div>
            <ul>
                <li v-for="element, index in navAfterImg" :key="'b' + index" >{{ element }}</li>
            </ul>
        </div>
        <div class="user-utilities flex">
            <div class="cart">
                <span>CART</span>
                <img src="../assets/svg/svg-1.svg" alt="">
                <div class="cart-number">0</div>
            </div>
            <div>SEARCH</div>
        </div>
    </nav>
    <div class="jumbotron">
        <img src="../assets/img/h3-rev-img-6.png" alt="jumbo-img">
    </div>
  </header>
</template>

<script>
export default {
    props: {
        navBeforeImg: Array,
        navAfterImg: Array,
    }
}
</script>

<style lang="scss" scoped>
    @import '../assets/scss/vars.scss';
    @import '../assets/scss/style.scss';
    
    header {
        background-image: url(../assets/img/h3-rev-img-5.png);
        background-repeat: no-repeat;
        background-position: center;
        background-color: $bg-black-2;
        color: $txt-white-1;
        font-weight: 400;
        font-size: 11px;
        letter-spacing: 3px;


        nav {
            width: 70%;
            margin: 0 auto;
            justify-content: space-between;
            align-items: center;

            .btn {
                width: 25%;

                button {
                    padding: 14px 28px;
                    background-color: $bg-red-3;
                    color: $txt-white-1;
                    font-family: inherit;
                    font-size: inherit;
                    letter-spacing: 4px;
                    cursor: pointer;
                    border-color: $border-red;
                }
            }

            .list {
                flex-shrink: 1;
                justify-self: center;
                width: 50%;
                justify-content: center;
                align-items: center;
                height: 100%;
                padding: 0 20px;

                ul {
                    flex-grow: 1;
                    display: flex;
                    justify-content: space-evenly;
                }

                img {
                    flex-shrink: 1;
                    height: 150px;
                    padding: 25px;
                }

                .home {
                    position: relative;

                    li:first-child::before {
                        content: url(../assets/svg/svg-0.svg);
                        filter: invert(1);
                        position: absolute;
                        top: 0;
                        left: -12px;
                        width: 20px;
                    }
                }
            }

            .user-utilities {
                width: 25%;
                justify-content: center;

                div {
                    padding: 0 10px;
                }

                .cart {
                    position: relative;

                    img {
                        width: 27px;
                        position: absolute;
                        top: -3px;
                        left: -24px;
                        filter: invert(1);
                    }

                    .cart-number {
                        position: absolute;
                        top: -5px;
                        left: -30px;
                        width: 15px;
                        height: 15px;
                        padding: 0;
                        text-align: center;
                        line-height: 15px;
                        padding-left: 2px;
                        border-radius: 50%;
                        background-color: $bg-white-1;
                        color: $txt-red-1;
                    }
                }
            }
        }

        .jumbotron {
            text-align: center;
            padding: 20px 0 70px;

            img {
                width: auto;
                height: 100%;
                display: inline-block;
            }
        }
    }
</style>