<template>
  <div class="page">
    <GameTitle/>
    <div class="text">
      hi
    </div>
  </div>
</template>

<script>
import GameTitle from '@/components/GameTitle.vue';

export default {
  name: 'GameContainer',
  components: {
    GameTitle,
  },
};
</script>

<style lang="scss">
@import '@/scss/main.scss';
</style>
