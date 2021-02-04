<!-- layout -->
<template>
  <div class="app">
    <Hero
      header="Let's create good vibes."
      subheadSm="The web is a messy place—it can be overwhelming and disorganized. We believe there's a better way to save, group, and share vibes."
      subheadMd="The web is a messy place—it can be overwhelming and disorganized. We believe there's a better way to save, group, and share vibes (and of course, cat videos)."
    />
    <ProductPreview />
    <SectionDarkMode />
    <SectionToolbox />
    <Footer />
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
import Footer from "~/components/Footer";
Footer;
export default {
  head: () => ({
    title: "home",
  }),
  components: { Hero, ProductPreview, SectionToolbox, SectionDarkMode, Footer },
  mounted() {},
};
</script>
