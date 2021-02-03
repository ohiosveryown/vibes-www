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

    <span class="blur" />
    <span class="layer layer-1" />
    <span class="layer layer-2" />
    <span class="layer layer-3" />
  </footer>
</template>

<!-- style -->
<style lang="scss" scoped>
@import "~/static/style/grid.scss";
.blur {
  position: absolute;
  z-index: var(--zmin);
  width: 100%;
  height: 100%;
  backdrop-filter: blur(100px);
}
.layer {
  position: absolute;
  z-index: -999999;
  top: 40rem;
  bottom: 0;
  border-radius: 100%;
}
.layer-1 {
  width: 100%;
  height: 37.6rem;
  transform: rotate(-15deg) translateY(-4rem);
  background: linear-gradient(
    132.08deg,
    #964eb7 0.76%,
    #f090bd 29.45%,
    #d8c8fa 67.13%
  );
}

.layer-2 {
  width: 100%;
  height: 37.6rem;
  transform: rotate(-0deg) translateX(10vw);
  background: linear-gradient(180deg, #413dae 0%, #7076cf 100%);
}

.layer-3 {
  width: 100%;
  height: 20rem;
  transform: rotate(-0deg) translateX(0vw);
  background: linear-gradient(105.3deg, #f0449f 1.34%, #f7a080 100%);
}

footer {
  overflow: hidden;
  display: flex;
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
