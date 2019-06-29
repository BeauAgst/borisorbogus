<template>
  <div class="page">
    <GameTitle/>

    <div class="text">
      <p>Currently stationed as our
        <strong>'Secretary of State for Foreign and Commonwealth Affairs'</strong>,
        <a rel="noopener noreferrer nofollow" target="_blank" href="https://en.wikipedia.org/wiki/Boris_Johnson">Boris Johnson</a>
        has made some pretty outlandish and controversial statements throughout the years.
      </p>
      <p>
        Can you guess which of the following quotes can be attributed to Boris?
        And which ones are just flat-out bogus?
      </p>
    </div>

    <button @click=startGame>Play</button>
  </div>
</template>

<script>
import GameTitle from '@/components/GameTitle.vue';

export default {
  name: 'IntroContainer',
  components: {
    GameTitle,
  },
  methods: {
    startGame() {
      this.$emit('onGameStart');
    },
  },
};
</script>

<style lang="scss">
@import '@/scss/main.scss';
</style>
