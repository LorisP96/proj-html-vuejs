<template>
  <div id="app">
    <div class="slice">
      <img src="./assets/svg/svg-4.svg" alt="">
    </div>
    <HeaderComponent :navBeforeImg='navBeforeImg' :navAfterImg='navAfterImg' />
    <MainComponent :pizzaMenu='pizzaMenu' :socialIcon='socialIcon'/>
    <FooterComponent :socialIcon='socialIcon'/>
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import MainComponent from './components/MainComponent.vue';
import FooterComponent from './components/FooterComponent.vue';


export default {
  name: 'App',
  components: {
    HeaderComponent,
    MainComponent,
    FooterComponent,
  },
  data(){
    return {
    navBeforeImg: ['HOME','PAGES','MENU'],
    navAfterImg: ['EVENT','BLOG','LANDING'],
    pizzaMenu: [
      {
        img: require('./assets/img/h3-product-img-1a-100x100.png'),
        name: 'BISMARCK',
        price: '$30.00',
        oldPrice: '$55.00'
      },
      {
        img: require('./assets/img/h3-product-img-2a-150x150.png'),
        name: 'FIORI DI ZUCCA',
        price: '$7.00 - $50.00',
        oldPrice: ''
      },
      {
        img: require('./assets/img/h3-product-img-3a-150x150.png'),
        name: 'VALDOSTANA',
        price: '$55.00',
        oldPrice: ''
      },
      {
        img: require('./assets/img/h3-product-img-4a-150x150.png'),
        name: 'PIZZA TARTUFATA',
        price: '$45.00',
        oldPrice: ''
      },
      {
        img: require('./assets/img/h3-product-img-5a-150x150.png'),
        name: 'FRANCESCANA',
        price: '$25.00',
        oldPrice: ''
      },
      {
        img: require('./assets/img/h3-product-img-6a-100x100.png'),
        name: 'CAMPAGNOLA',
        price: '$50.00 - $95.00',
        oldPrice: ''
      },
    ],
    socialIcon: {
        Twitter: "fa-brands fa-twitter",
        Facebook: "fa-brands fa-facebook-f",
        Instagram: "fa-brands fa-instagram",
        LinkedIn: "fa-brands fa-linkedin-in",
      },
    }
  } 
}
</script>

<style lang="scss">
@import './assets/scss/vars.scss';
@import './assets/scss/style.scss';
@import url('https://fonts.googleapis.com/css2?family=Fredoka:wght@300;400;700&family=Montserrat:wght@300;400;700&family=Nunito+Sans:wght@300;600&family=Open+Sans:wght@500;700&family=Oswald:wght@200;300;400&family=PT+Sans:wght@400;700&family=Raleway&family=Rock+Salt&family=WindSong:wght@400;500&display=swap');
#app {
  font-family: 'Oswald', sans-serif;
  color: $txt-black-4;
  letter-spacing: 1.2px;

  .slice {
    position: fixed;
    bottom: 25px;
    right: 25px;
    width: 40px;
    height: 40px;
    border-radius: 50%;
    background-color: $bg-white-3;
    display: flex;
    justify-content: center;
    img {
        width: 16px;
    }
    z-index: 1;
  }
}
</style>
