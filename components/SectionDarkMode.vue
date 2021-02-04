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
      <h4 class="mb-2 font-prim">So, what exactly is it now?</h4>
      <p class="font-body">
        You can think of the Vibes app as a DVR for the internet
        – remember&nbsp;those?
      </p>
      <p class="font-body">
        Save articles, videos, audio, and stories from any publication, page, or
        app. Curate your own space, or collaborate and share with&nbsp;others.
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
  margin: 4.8rem auto 0;
  padding: 1.2rem 0 0;
  min-height: 10rem;
  background: linear-gradient(104deg, #eeaeca 2%, #94bbe9 100%);
  overflow: hidden;
  @include breakpoint(md) {
    margin-top: 8rem;
    padding: 2.4rem 0 0;
    width: grid-width(10);
  }
  @include breakpoint(mdl) {
    padding: 2.4rem 0 0;
  }
}

img {
  margin: auto;
}

article {
  margin: 0 auto;
  text-align: center;
  @include breakpoint(md) {
    padding-top: 11.2rem;
    width: grid-width(8.4);
  }
}

h4 {
  font-size: 3.2rem;
  @include breakpoint(md) {
    font-size: 3.8vw;
  }
}

p {
  margin-bottom: 2rem;
  @include breakpoint(md) {
    font-size: 2.2rem;
  }
}
</style>

<!-- logic -->
<script>
export default {
  mounted() {},
};
</script>
