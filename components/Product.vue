<!-- layout -->
<template>
  <section>
    <video autoplay="autoplay" playsinline="" loop="loop">
      <source
        src="https://res.cloudinary.com/da32ufmnf/video/upload/v1597081255/blush/blush_d2t8sk.mp4"
      />
      <source />
    </video>
    <img
      class="bg"
      src="../static/img/bg@2x.png"
      alt="gradient background image"
    />
    <div class="clusters">
      <img
        class="cluster c1"
        src="../static/img/cluster-01@2x.png"
        alt="avatars"
      />
      <img
        class="cluster c2"
        src="../static/img/cluster-02-2@2x.png"
        alt="avatars"
      />
      <img
        class="cluster c3"
        src="../static/img/cluster-03@2x.png"
        alt="avatars"
      />
      <img
        class="cluster c4"
        src="../static/img/cluster-04@2x.png"
        alt="avatars"
      />
      <img
        class="cluster c5"
        src="../static/img/cluster-05@2x.png"
        alt="avatars"
      />
      <img
        class="cluster c6"
        src="../static/img/cluster-06@2x.png"
        alt="avatars"
      />
    </div>
  </section>
</template>

<!-- style -->
<style lang="scss" scoped>
@import "~/static/style/grid.scss";
section {
  position: relative;
}

video {
  margin: 0 auto;
  max-width: var(--max-width);
  width: 90vw;
  @include breakpoint(md) {
    width: grid-width(9.5);
  }
}

.bg {
  position: absolute;
  z-index: var(--zmin);
  top: 0rem;
  pointer-events: none;
  @include breakpoint(md) {
    top: -20rem;
  }
}

.clusters {
  display: flex;
  justify-content: space-between;
  width: 100vw;
  overflow-x: hidden;
}

.cluster {
  width: 16rem;
  height: auto;
}

.cluster:nth-of-type(1) {
  margin-left: -2.4rem;
}

.cluster:nth-of-type(2) {
}

.cluster:nth-of-type(6) {
  margin-right: -2.4rem;
}
</style>

<!-- logic -->
<script>
export default {
  // props: [ 'header', 'subhead' ],
  mounted() {
    const randomX = random(1, 10);
    const randomY = random(1, 10);
    const randomDelay = random(0, 1);
    const randomTime = random(3, 5);
    const randomTime2 = random(5, 10);
    const randomAngle = random(-10, 10);

    const cans = gsap.utils.toArray(".cluster");
    cans.forEach((can) => {
      gsap.set(can, {
        x: randomX(-1),
        y: randomX(1),
      });

      moveX(can, 1);
      moveY(can, -1);
    });

    function moveX(target, direction) {
      gsap.to(target, randomTime(), {
        x: randomX(direction),
        ease: Sine.easeInOut,
        onComplete: moveX,
        onCompleteParams: [target, direction * -1],
      });
    }

    function moveY(target, direction) {
      gsap.to(target, randomTime(), {
        y: randomY(direction),
        ease: Sine.easeInOut,
        onComplete: moveY,
        onCompleteParams: [target, direction * -1],
      });
    }

    function random(min, max) {
      const delta = max - min;
      return (direction = 1) => (min + delta * Math.random()) * direction;
    }
  },
};
</script>
