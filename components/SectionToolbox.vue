<!-- layout -->
<template>
  <section class="width">
    <figure>
      <img src="https://res.cloudinary.com/da32ufmnf/image/upload/v1614713882/vibes-www/toolbox_2x_m6oq9q.png" alt="toolbox search and filter">
      <!-- <video
        preload="metadata"
        playsinline=""
        muted
        loop="loop"
        controls="true"
        poster="https://res.cloudinary.com/da32ufmnf/image/upload/v1614713255/vibes-www/toolbox-poster_2x_kmgsmo.jpg"
      >
        <source
          src="https://res.cloudinary.com/da32ufmnf/video/upload/v1614713257/vibes-www/toolbox_pwxtkw.mp4"
        />
        <source />
      </video> -->
    </figure>

    <article class="pb-0">
      <h4 class="mb-2 font-prim">It’s a Vibe.</h4>
      <p class="font-body">
        Vibes brings clarity and organization to the internet without likes,
        vanity, and distraction. That means no ads, no data harvesting, no
        influencers, no algorithms and no&nbsp;distractions.
      </p>
      <p class="font-body">Tune out the noise and let clarity&nbsp;in.</p>
    </article>
  </section>
</template>

<!-- style -->
<style lang="scss" scoped>
@import "~/static/style/grid.scss";
figure {
  margin: 0 auto 4rem;
  padding: 4.8rem 0;
  min-height: 10rem;
  background: linear-gradient(248deg, #eeaeca -16%, #94bbe9 134%);
  overflow: ￼;
  @include breakpoint(md) {
    margin-top: 2.4rem;
    padding: 8rem 0 6rem;
    width: grid-width(10);
  }
  // @include breakpoint(mdl) {
  //   padding: 8rem 0 6rem;
  // }
}

video {
  margin: auto;
  width: 80%;
  box-shadow: 0px 22px 44px rgba(0, 0, 0, 0.24);
  border-radius: 10px;
}

article {
  margin: 0 auto;
  text-align: center;
  @include breakpoint(md) {
    padding-top: 2.4rem;
    width: grid-width(8.4);
  }
  @include breakpoint(mdl) {
    padding-top: 6.4rem;
    width: grid-width(8.4);
  }
}

h4 {
  font-size: 3.2rem;
  @include breakpoint(md) {
    padding-bottom: 1.6rem;
    font-size: 5.6vw;
  }
  @include breakpoint(mdl) {
    padding-bottom: 0;
    font-size: 3.8vw;
  }
}

p {
  margin-bottom: 2rem;
  font-size: 1.6rem;
  @include breakpoint(md) {
    font-size: 2.1rem;
  }
}
</style>

<!-- logic -->
<script>
export default {
  mounted() {},
};
</script>
