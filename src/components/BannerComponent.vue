<template>
    <section class="banner">
        <div class="banner-in-banner" id="top-banner"></div>
        <div class="banner-in-banner" id="mid-banner"></div>
        <div class="banner-in-banner" id="bot-banner"></div>
        <h2>GO AHEAD AND<br>BUILD YOUR<br>OWN PIZZA<br>WE WON'T<br>JUDGE!</h2>
    </section>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
@import '../assets/scss/vars.scss';
@import '../assets/scss/style.scss';

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
        font-size: 60px;
        line-height: 60px;
    }
}
</style>