<!-- layout -->
<template>
  <div class="app">
    <Hero
      header="Tidying up the internet so teams and individuals can stay focused."
      subhead="The web is a messy place—it can be overwhelming and disorganized. We believe there's a better way to save, group, and share vibes (oh, and cat videos)."
    />
    <ProductPreview />
    <SectionToolbox />
    <SectionDarkMode />
  </div>
</template>

<!-- style -->
<style lang="scss" scoped>
@import "~/static/style/grid.scss";
</style>

<!-- logic -->
<script>
import Hero from "~/components/Hero";
import ProductPreview from "~/components/ProductPreview";
import SectionToolbox from "~/components/SectionToolbox";
import SectionDarkMode from "~/components/SectionDarkMode";
export default {
  head: () => ({
    title: "home",
  }),
  components: { Hero, ProductPreview, SectionToolbox, SectionDarkMode },
  mounted() {},
};
</script>
