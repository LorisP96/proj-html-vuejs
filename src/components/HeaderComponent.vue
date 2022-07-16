<template>
  <header>
    <nav class="flex">
        <div class="btn">
            <button>ORDER ONLNE</button>
        </div>
        <div class="list flex">
            <ul v-for="element, index in navBeforeImg" :key="'a' + index">{{element}}</ul>
            <div class="logo">
                <img src="../assets/img/h5-logo-divided-header.png" alt="logo">
            </div>
            <ul v-for="element, index in navAfterImg" :key="'b' + index">{{element}}</ul>
        </div>
        <div class="user-utilities flex">
            <div class="cart">CART</div>
            <div class="search">SEARCH</div>
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
            }

            .user-utilities {
                width: 25%;
                justify-content: center;

                div {
                    padding: 0 10px;
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