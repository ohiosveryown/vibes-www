<!-- layout -->
<template>
  <footer>
    <article class="width">
      <Icon class="mb-9" />
      <Form class="mt-4 mb-4" />
      <p class="mb-3 tac font-body">
        Sign up to get notified when Vibes is ready for release; currently
        estimating for the first quarter of 2021.
      </p>
      <h5 class="font-sec">
        <a
          target="_blank"
          href="https://twitter.com/cmykw_/status/1196273185987211264"
          >Follow Updates on Twitter</a
        >
      </h5>
    </article>

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
  position: relative;
  margin-top: 8rem;
  width: 100%;
  @include breakpoint(md) {
    margin-top: 16rem;
  }
}

article {
  display: flex;
  position: relative;
  flex-direction: column;
  align-items: center;
}

p {
  font-size: 1.6rem;
  @include breakpoint(md) {
    font-size: 1.8rem;
    width: grid-width(6);
  }
}

h5 {
  margin: 4rem 0;
  font-size: 1.4;
  color: var(--gravity);
  opacity: 1;
  @include breakpoint(md) {
    color: #fff;
  }
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

  mounted() {},
};
</script>
