<template>
  <footer>
    <!-- BOOKING -->
    <div class="booking">
        <div class="book-cont flex">
            <div class="book-card flex">
                <div class="user-input">1 Person</div>
                <div class="card-child">FOR</div>
            </div>
            <div class="book-card flex">
                <div class="user-input">11/29/2020</div>
                <div class="card-child">AT</div>
            </div>
            <div class="book-card flex">
                <div class="user-input">1 Person</div>
                <div class="card-child"></div>
            </div>
            <div class="book-card">
                <button>BOOK A TABLE</button>
            </div>
        </div>
    </div>
  </footer>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
@import '../assets/scss/vars.scss';
@import '../assets/scss/style.scss';

.booking {
    background-image: url(../assets/img/h3-background-img-3.jpg);
    padding: 90px;
    background-position: -120px;

    .book-cont {
        width: 60%;
        margin: 0 auto;
        line-height: 50px;

        .book-card {
            width: 25%;
            justify-content: space-between;
            color: $txt-white-1;

            .card-child {
                width: 25%;
                text-align: center;
            }

            .user-input {
                height: 50px;
                padding-block: 10px;
                padding-inline: 20px;
                line-height: 30px;
                background-color: $fill-white;
                width: 75%;
                color: $txt-grey-3;
                font-size: 11px;
                border: 1px solid $border-black;
            }

            button {
                width: 75%;
                height: 100%;
                display: block;
                font-family: inherit;
                letter-spacing: 1px;
                font-size: 11px;
                background-color: $bg-red-3;
                color: inherit;
                border: 0;
            }
        }
    }
}
</style>