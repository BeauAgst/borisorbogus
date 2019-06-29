<template>
  <div id="app">
    <IntroContainer
      v-if="!gameInProgress"
      @onGameStart="onGameStart"
    />
    <GameContainer v-if="gameInProgress"/>
    <PageFooter/>
  </div>
</template>

<script>
import IntroContainer from './components/IntroContainer.vue';
import GameContainer from '@/components/GameContainer.vue';
import PageFooter from './components/PageFooter.vue';

export default {
  name: 'app',
  components: {
    IntroContainer,
    GameContainer,
    PageFooter,
  },
  methods: {
    onGameStart() {
      this.gameInProgress = true;
    },
  },
  data() {
    return {
      gameInProgress: false,
    };
  },
};
</script>

<style lang="scss">
@import '@/scss/main.scss';
</style>
