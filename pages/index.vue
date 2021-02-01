<!-- layout -->
<template>
  <main class="width">
    <header>
      <Icon class="mt-9 mb-7"/>
      <h1 class="mb-2 font-prim">Tidying up the internet so teams and individuals can stay focused.</h1>
      <h2 class="font-body">The web is a messy place—it can be overwhelming and disorganized. We believe there's a better way to save, group, and share vibes (oh, and cat videos).</h2>
    </header>
  </main>
</template>

<!-- style -->
<style lang="scss" scoped>
  @import '~/static/style/grid.scss';

  .wrapper {
    border: 4px solid green;
    position: relative;
    margin: 0 auto;
  }

  header {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin: 0 auto;
    h1, h2 { text-align: center; }
    h1 {
      font-size: 4rem;
      line-height: 1.2;
      @include breakpoint(mdl) { font-size: 6.4rem; }
    }
    h2 {
      max-width: 56ch;
      font-size: 1.8rem;
      @include breakpoint(mdl) { font-size: 2rem; }
    }
  }
</style>

<!-- logic -->
<script>
  import Icon from '~/components/Icon'
  export default {
    head: () => ({
      title: 'home'
    }),
    components: { Icon, },
    mounted() {
      // gsap.from('.anim--enter', {
      //   opacity: 0,
      //   y: 200,
      //   skewY: 10,
      //   stagger: .15,
      //   duration: 1,
      //   ease: Power4.easeInOut
      // })
    }
  }
</script>
