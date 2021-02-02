<!-- layout -->
<template>
  <div class="app">
    <Hero
      header="Tidying up the internet so teams and individuals can stay focused."
      subhead="The web is a messy place—it can be overwhelming and disorganized. We believe there's a better way to save, group, and share vibes (oh, and cat videos)."
    />
    <Product />
  </div>
</template>

<!-- style -->
<style lang="scss" scoped>
@import "~/static/style/grid.scss";
</style>

<!-- logic -->
<script>
import Hero from "~/components/Hero";
import Product from "~/components/Product";
export default {
  head: () => ({
    title: "home",
  }),
  components: { Hero, Product },
  mounted() {},
};
</script>
