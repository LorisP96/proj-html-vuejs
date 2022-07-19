<template>
    <section class="intro flex">
        <div class="intro-card">
            <img src="../assets/img/h3-img-1.jpg" alt="">
            <div class="select-img">
                <div class="eye flex"><i class="fa-solid fa-eye"></i></div>
            </div>
        </div>
        <div class="intro-card">
            <img src="../assets/img/h3-img-2.jpg" alt="">
            <div class="select-img">
                <div class="eye flex"><i class="fa-solid fa-eye"></i></div>
            </div>
        </div>
        <div class="intro-card">
            <img src="../assets/img/h3-img-3.jpg" alt="">
            <div class="select-img">
                <div class="eye flex"><i class="fa-solid fa-eye"></i></div>
            </div>
        </div>
        <div class="intro-card">
            <img src="../assets/img/h3-img-4.jpg" alt="">
            <div class="select-img">
                <div class="eye flex"><i class="fa-solid fa-eye"></i></div>
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

.intro {
    padding: 8px 0;
    justify-content: space-between;

    .intro-card {
        width: calc((100% / 4) - 8px);

        .select-img {
            height: 100%;
            display: none;
            justify-content: center;
            align-items: center;
            position: relative;

            &::before {
                content: "";
                background-image: url('https://i.pinimg.com/originals/be/f3/86/bef386ecd3ddea8424067f7c0c2048c5.png');
                background-size: cover;
                position: absolute;
                top: 0px;
                right: 0px;
                bottom: 0px;
                left: 0px;
                opacity: 0.25;
            }


            .eye {
                width: 80px;
                height: 80px;
                border-radius: 50%;
                background-color: $bg-red-3;
                color: $txt-white-1;
                align-items: center;
                justify-content: center;
                font-size: 20px;
                z-index: 1;
            }
        }

        &:hover {
            img {
                display: none;
            }

            .select-img {
                display: flex;


            }
            
        }
    }
}
</style>