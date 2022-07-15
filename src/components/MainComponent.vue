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
        background-image: url('../assets/img/h3-testimonials-bckgrnd.jpg');
        margin-bottom: 6px;
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
</style>