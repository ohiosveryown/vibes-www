<!-- layout -->
<template>
  <main>
    <h1 class="skw anim--enter mb-4 font-prim">Proportional.design</h1>
    <Article class="skw anim--enter"/>
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
    components: { Article, },
    mounted() {
      gsap.from('.anim--enter', {
        opacity: 0,
        y: 200,
        skewY: 10,
        stagger: .15,
        duration: 1,
        ease: Power4.easeInOut
      })
    }
  }
</script>
