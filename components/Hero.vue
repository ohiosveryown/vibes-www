<!-- layout -->
<template>
  <header class="width">
    <Icon class="mt-9 mb-7"/>
    <h1 class="mb-2 font-prim">{{ header }}</h1>
    <h2 class="font-body">{{ subhead }}</h2>
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
    components: { Icon, },
    props: [ 'header', 'subhead' ],
  }
</script>