<!-- layout -->
<template>
  <header class="width">
    <Icon class="mt-7 mb-5"/>
    <h1 class="enter mb-2 font-prim">{{ header }}</h1>
    <h2 class="enter mb-5 font-body">{{ subhead }}</h2>
    <Form class="enter"/>
  </header>
</template>

<!-- style -->
<style lang="scss" scoped>
  @import '~/static/style/grid.scss';
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
      @include breakpoint(md) { font-size: 5vw; }
      // @include breakpoint(mdl) { font-size: 6.4rem; }
      // @include breakpoint(lg)  { font-size: 7rem; }
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
  import Form from '~/components/Form'
  export default {
    components: { Icon, Form },
    props: [ 'header', 'subhead' ],
    
    mounted() {
      // gsap.from('.enter', {
      //   opacity: 0,
      //   duration: 3,
      //   delay: .3,
      //   ease: "elastic.out(1,.5)"
      // })
    }
  }
</script>