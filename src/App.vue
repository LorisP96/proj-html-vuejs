<template>
  <div id="app">
    <HeaderComponent :navBeforeImg='navBeforeImg' :navAfterImg='navAfterImg' />
    <MainComponent/>
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import MainComponent from './components/MainComponent.vue';


export default {
  name: 'App',
  components: {
    HeaderComponent,
    MainComponent,
  },
  data(){
    return {
    navBeforeImg: ['HOME','PAGES','MENU'],
    navAfterImg: ['EVENT','BLOG','LANDING'],
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
  letter-spacing: 3px;
}
</style>
