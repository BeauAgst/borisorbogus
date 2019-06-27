<template>
  <div id="app">
    <IntroContainer/>
    <PageFooter/>
  </div>
</template>

<script>
import IntroContainer from './components/IntroContainer.vue';
import PageFooter from './components/PageFooter.vue';

export default {
  name: 'app',
  components: {
    IntroContainer,
    PageFooter,
  },
};
</script>

<style lang="scss">
@import '@/scss/main.scss';
</style>
