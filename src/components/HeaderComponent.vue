<template>
  <header>
    <nav class="flex">
        <div class="btn">
            <button>ORDER ONLNE</button>
        </div>
        <div class="list flex">
            <ul v-for="element, index in navBeforeImg" :key="index">{{element}}</ul>
            <div class="logo">
                <img src="../assets/img/h5-logo-divided-header.png" alt="logo">
            </div>
            <ul v-for="element, index in navAfterImg" :key="index">{{element}}</ul>
        </div>
        <div class="user-utilities">
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
    data() {
        return {
            navBeforeImg: ['HOME','PAGES','MENU'],
            navAfterImg: ['EVENT','BLOG','LANDING']
        }
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
        font-size: 14px;
        letter-spacing: 4px;
        nav {
            width: 70%;
            margin: 0 auto;
            justify-content: space-between;
            align-items: center;

            .btn {

                padding: 0 25px;

                button {
                    padding: 18px 32px;
                    background-color: $bg-red-3;
                    color: $txt-white-1;
                    font-family: inherit;
                    letter-spacing: 4px;
                }
            }

            .list {
                flex-grow: 1;
                justify-content: center;
                align-items: center;
                height: 100%;
                padding: 0 40px;

                ul {
                    flex-grow: 1;
                    display: flex;
                    justify-content: space-around;
                }

                img {
                    flex-shrink: 1;
                    height: 170px;
                    padding: 25px 0;
                }
            }

            .user-utilities {
                div {
                    display: inline-block;
                    padding: 0 25px;
                }
            }
        }

        .jumbotron {
            text-align: center;
            padding: 20px 0 70px;
        }
    }
</style>