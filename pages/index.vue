<!-- layout -->
<template>
  <main>
    <h1 class="mb-4 font-prim">Hello World – with nuxt and gsap</h1>
    <Article/>
  </main>
</template>

<!-- style -->
<style lang="scss" scoped>
  @import '~/static/style/grid.scss';

  h1 {
    color: pink;
    @include breakpoint(mdl) { color: tan; }
  }
</style>

<!-- logic -->
<script>
  import Article from '~/components/Article'
  export default {
    head: () => ({
      title: 'home'
    }),
    components: { Article, }
  }
</script>