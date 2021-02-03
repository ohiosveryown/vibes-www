<!-- layout -->
<template>
  <section class="width pb-9">
    <figure class="mb-9">
      <img
        src="https://res.cloudinary.com/da32ufmnf/image/upload/v1612319245/vibes-www/darkmode_ktkn3b.png"
        alt="Vibe app dark mode and light mode"
      />
    </figure>

    <article class="pb-0">
      <h4 class="mb-2 font-prim">It’s a Vibe.</h4>
      <p class="font-body">
        Vibes brings clarity and organization to the internet without likes,
        vanity, and distraction. That means no ads, no data harvesting, no
        influencers, no algorithms and no&nbsp;distractions.
      </p>
      <p class="font-body">
        Once you have your Vibes saved, use Toolbox to easily find, filter, and
        reference your content for simple recollection and&nbsp;reception.
      </p>
    </article>
  </section>
</template>

<!-- style -->
<style lang="scss" scoped>
@import "~/static/style/grid.scss";
figure {
  margin-top: 4.8rem;
  padding: 1.2rem 0 0;
  min-height: 10rem;
  background: linear-gradient(104deg, #eeaeca 2%, #94bbe9 100%);
  overflow: hidden;
  @include breakpoint(md) {
    margin-top: 8rem;
    padding: 2.4rem 0 0;
  }
  @include breakpoint(mdl) {
    padding: 2.4rem 0 0;
  }
}

img {
  margin: auto;
  // width: 80%;
  // box-shadow: 0px 22px 44px rgba(0, 0, 0, 0.24);
  // border-radius: 10px;
}

article {
  margin: 0 auto;
  text-align: center;
  p {
    margin-bottom: 2rem;
  }
  @include breakpoint(md) {
    width: grid-width(8.4);
  }
}

h4 {
  font-size: 3.2rem;
  @include breakpoint(md) {
    font-size: 3.2rem;
  }
}
</style>

<!-- logic -->
<script>
export default {
  mounted() {},
};
</script>
