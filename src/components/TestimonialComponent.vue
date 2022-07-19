<template>
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
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
@import '../assets/scss/vars.scss';
@import '../assets/scss/style.scss';

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
</style>