<template>
  <div class="game-title">
    <div>
      <span>Boris</span>
    </div>
    <div>
      <span>or</span>
    </div>
    <div>
      <span>Bogus</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'GameTitle',
};
</script>

<style lang="scss">
.game-title {
  display: inline-block;
  position: relative;
  z-index: 1;
  line-height: 1;
  font-size: 8vw;
  background: $color--primary;
  border-radius: .1em;
  box-shadow: 2px 1px 19px rgba(0, 0, 0, 0.15);
  margin-bottom: 20px;

  div {
    display: inline-block;
    vertical-align: top;
    padding: 0.05em .2em;
    border-radius: .2em;
    letter-spacing: -0.01em;
    line-height: 1;
    color: #fff;
    text-transform: uppercase;
    font-weight: 900;
    background: $color--primary;
  }

  span {
    display: inline-block;
    vertical-align: top;
    line-height: 1;
  }
}

@media (max-width: 767px) and (orientation: portrait) {
  .game-title {
    font-size: 10vw;

    div {
      display: block;
    }
  }
}

@media (min-width: 1200px) {
  .game-title {
    font-size: 96px;
  }
}
</style>
