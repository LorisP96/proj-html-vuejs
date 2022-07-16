<template>
  <div id="app">
    <HeaderComponent :navBeforeImg='navBeforeImg' :navAfterImg='navAfterImg' />
    <MainComponent :pizzaMenu='pizzaMenu' />
    <FooterComponent/>
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
    ]
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
}
</style>
