<template>
    <section class="hello">  
        <div class="washington-review flex">
            <div class="quot-hello"><i class="fa-solid fa-quote-left"></i></div>
            <h3>"FORGET THE TRENDY PIZZA SHOPS, THIS HIDDEN SPOT MAKES THE BEST NEW YORK-STYLE PIZZA SLICE IN NAPLES"</h3>
            <h6>WASHINGTON POST 2018</h6>
            <div class="dots flex">
                <i class="fa-solid fa-circle"></i>
                <i class="fa-solid fa-circle"></i>
                <i class="fa-solid fa-circle"></i>
            </div>
        </div>

        <div class="next">NEXT</div>
        <div class="prev">PREV</div>
    </section>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
@import '../assets/scss/vars.scss';
@import '../assets/scss/style.scss';

.hello {
    height: 495px;
    background-image: url(../assets/img/h3-testimonials-bckgrnd.jpg);
    background-position: -100px ;
    position: relative;

    .washington-review {
        justify-content: center;
        align-items: center;
        flex-direction: column;
        height: 100%;
        width: 40%;
        margin: 0 auto;
        text-align: center;
        line-height: 31px;

        .quot-hello {
            font-size: 75px;
            color: $txt-gold-1;
            padding-bottom: 15px;
        }

        .dots {
            color: $txt-white-2;
            padding-top: 25px;
            font-size: 7px;
            align-items: center;
            
            i {
                padding-inline: 3px;

                &:first-child {
                    font-size: 9px;
                    color: $txt-gold-1;
                }
            }
        }
    }

    .next, .prev {
        top: 50%;
        padding-left: 20px;
    }
}
</style>