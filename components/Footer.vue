<!-- layout -->
<template>
  <footer class="width">
    <Icon class="mt-7 mb-9" />
    <Form class="mt-4 mb-4" />
    <p class="mb-3 tac font-body">
      Sign up to get notified when Vibes is ready for release; currently
      estimating for the first quarter of 2021.
    </p>
    <h5 class="font-sec">
      <a target="_blank" href="https://twitter.com/cmykw_"
        >Follow Updates on Twitter</a
      >
    </h5>

    <img
      src="https://res.cloudinary.com/da32ufmnf/image/upload/v1612319533/vibes-www/bg-footer_mbxpa9.jpg"
      alt=""
      class="bg"
    />
  </footer>
</template>

<!-- style -->
<style lang="scss" scoped>
@import "~/static/style/grid.scss";
footer {
  display: flex;
  position: relative;
  overflow: hidden;
  flex-direction: column;
  align-items: center;
  position: relative;
  width: 100%;
}

p {
  @include breakpoint(md) {
    font-size: 1.6rem;
    width: grid-width(6);
  }
}

h5 {
  margin-bottom: 8rem;
  font-size: 1.4;
  opacity: 0.64;
}

.bg {
  position: absolute;
  z-index: var(--zmin);
  bottom: 0;
  width: 100vw;
  mix-blend-mode: multiply;
}
</style>

<!-- logic -->
<script>
import Icon from "~/components/Icon";
import Form from "~/components/Form";
export default {
  components: { Icon, Form },
  props: ["header", "subhead"],

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
