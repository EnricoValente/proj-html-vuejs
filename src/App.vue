<script>
    import HeaderComponent from './components/HeaderComponent.vue';
    import MainComponent from './components/MainComponent.vue';
    import FooterComponent from './components/FooterComponent.vue';
    import { store } from './store';

    export default {
    data() {
        return {
            store,
        }
    },
    components: {
        HeaderComponent,
        MainComponent,
        FooterComponent,
    }
    }
</script>


<template>
  <HeaderComponent />
  <MainComponent />
  <FooterComponent />
</template>

<style lang="scss">
@use "./assets/scss/main.scss"
</style>
