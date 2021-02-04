<!-- layout -->
<template>
  <header class="width">
    <Icon class="icon" />
    <h1 class="mb-2 font-prim">{{ header }}</h1>
    <h2 class="for-sm font-body">{{ subheadSm }}</h2>
    <h2 class="for-md font-body">{{ subheadMd }}</h2>
    <Form class="enter" />
  </header>
</template>

<!-- style -->
<style lang="scss" scoped>
@import "~/static/style/grid.scss";
header {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin: 0 auto 4rem;
  @include breakpoint(md) {
    margin-bottom: 8rem;
  }

  .icon {
    margin: 4.8rem 0 4rem;
    @include breakpoint(md) {
      margin: 5.6rem 0 4rem;
    }
  }

  h1,
  h2 {
    text-align: center;
  }
  h1 {
    font-size: 6rem;
    line-height: 1.1;
    @include breakpoint(md) {
      font-size: 7.2vw;
    }
  }
  h2 {
    margin-top: 1.2rem;
    margin: 1.2rem 0 4.8rem;
    font-size: 1.9rem;
    @include breakpoint(mdl) {
      margin-top: 0;
      margin: 0 0 6.4rem;
      max-width: 56ch;
      font-size: 2rem;
    }
  }
}

.for-sm {
  @include breakpoint(md) {
    display: none;
  }
}

.for-md {
  display: none;
  @include breakpoint(md) {
    display: inherit;
  }
}
</style>

<!-- logic -->
<script>
import Icon from "~/components/Icon";
import Form from "~/components/Form";
export default {
  components: { Icon, Form },
  props: ["header", "subheadSm", "subheadMd"],

  mounted() {
    // gsap.from('.enter', {
    //   opacity: 0,
    //   duration: 3,
    //   delay: .3,
    //   ease: "elastic.out(1,.5)"
    // })
  },
};
</script>
