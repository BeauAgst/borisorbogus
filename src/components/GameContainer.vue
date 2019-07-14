<template>
  <div class="page" id="page">
    <GameTitle/>
    <div class="text">
      <div class="quote">
        {{quote}}
      </div>
      <div class="context" v-if=answerSubmitted>
        {{quoteContext}}
      </div>
    </div>
    <div v-if=!answerSubmitted>
      <button @click=submitBoris()>Boris</button>
      or
      <button @click=submitBogus()>Bogus</button>
    </div>
    <button v-if=answerSubmitted @click=next()>Next</button>
  </div>
</template>

<script>
import GameTitle from '@/components/GameTitle.vue';
import allQuotes from '../data/allQuotes.json';

export default {
  name: 'GameContainer',
  components: {
    GameTitle,
  },
  data: () => ({
    quoteIndex: 0,
    answerSubmitted: false,
  }),
  computed: {
    quote() {
      return allQuotes.quotes[this.quoteIndex].quote;
    },
    quoteContext() {
      return allQuotes.quotes[this.quoteIndex].information;
    },
  },
  methods: {
    submitBoris() {
      this.answerSubmitted = true;
    },
    submitBogus() {
      this.answerSubmitted = true;
    },
    next() {
      this.quoteIndex = this.quoteIndex + 1;
      this.answerSubmitted = false;
    },
  },
};
</script>

<style lang="scss">
@import '@/scss/main.scss';

.quote {
  font-size: 28px;
}
.context {
  margin-top: 20px;
  font-size: 20px;
}
</style>
