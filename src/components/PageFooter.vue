<template>
  <footer>
    <div class="made-by">
      Made with &#10084; by
      <template v-for="(contributor, index) in contributors">
        <a
          :href="contributor.url"
          :key="contributor.name"
          class="made-by__name"
          rel="noopener noreferrer nofollow"
          target="_blank"
        >{{ contributor.name }}</a>
        {{ index === contributors.length -1 ? null : '&' }}
      </template>
    </div>
    <div class="other-links">
        <a rel="noopener" target="_blank" href="https://voteforpolicies.org.uk">Vote for policies</a> |
        <a href="#">Print-out Boris mask!</a>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'PageFooter',
  data() {
    return {
      contributors: [
        {
          name: 'Beau August',
          url: 'https://beaugust.co.uk',
        },
      ],
    };
  },
};
</script>

<style lang="scss">
footer {
  position: fixed;
  right: 0;
  bottom: 0;
  left: 0;
  text-align: center;
  padding: 20px;
  font-size: 13px;
}

@media (max-width: 767px) and (max-height: 639px) and (orientation: portrait) {
  footer {
    position: static;
  }
}
</style>
