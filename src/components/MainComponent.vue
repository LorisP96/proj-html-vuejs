<template>
  <main>
    
    <IntroComponent/>

    <HelloComponent/>

    <SpecialComponent/>

    <BannerComponent/>

    <TeamComponent :socialIcon='socialIcon'/>

    <TestimonialComponent/>

    <PizzaComponent :pizzaMenu='pizzaMenu'/>

    <DealComponent :socialIcon='socialIcon'/>

  </main>
</template>

<script>
import IntroComponent from './IntroComponent.vue';
import HelloComponent from './HelloComponent.vue';
import SpecialComponent from './SpecialComponent.vue';
import BannerComponent from './BannerComponent.vue';
import TeamComponent from './TeamComponent.vue';
import TestimonialComponent from './TestimonialComponent.vue';
import PizzaComponent from './PizzaComponent.vue';
import DealComponent from './DealComponent.vue';


export default {
    props: {
        pizzaMenu: Array,
        socialIcon: Object,
    },
    components: {
    HelloComponent,
    SpecialComponent,
    IntroComponent,
    BannerComponent,
    TeamComponent,
    TestimonialComponent,
    PizzaComponent,
    DealComponent
}
}
</script>

<style lang="scss" scoped>
    @import '../assets/scss/vars.scss';
    @import '../assets/scss/style.scss';
</style>