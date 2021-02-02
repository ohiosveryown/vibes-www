<!-- layout -->
<template>
  <section>
    <!-- <video autoplay="autoplay" playsinline="" loop="loop">
      <source
        src="https://res.cloudinary.com/da32ufmnf/video/upload/v1597081255/blush/blush_d2t8sk.mp4"
      />
      <source />
    </video> -->

    <img src="../static/img/delete@2x.png" alt="" class="delete" />

    <div class="bubbles">
      <figure>
        <img
          class="bubble bubble-01"
          src="../static/img/bubble-01c.png"
          alt="Vibe Group"
        />
      </figure>

      <figure>
        <img
          class="bubble bubble-02"
          src="../static/img/bubble-02.png"
          alt="Vibe Group"
        />
      </figure>

      <figure>
        <img
          class="bubble bubble-03"
          src="../static/img/bubble-03.png"
          alt="Vibe Group"
        />
      </figure>

      <figure>
        <img
          class="bubble bubble-04"
          src="../static/img/bubble-04.png"
          alt="Vibe Group"
        />
      </figure>

      <figure>
        <img
          class="bubble bubble-05"
          src="../static/img/bubble-05.png"
          alt="Vibe Group"
        />
      </figure>

      <figure>
        <img
          class="bubble bubble-06"
          src="../static/img/bubble-06.png"
          alt="Vibe Group"
        />
      </figure>
    </div>

    <img src="../static/img/bg@2x.png" alt="" class="bg" />
  </section>
</template>

<!-- style -->
<style lang="scss" scoped>
@import "~/static/style/grid.scss";
section {
  position: relative;
}

video,
.delete {
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
  top: 0;
}

.bubbles {
  display: flex;
  justify-content: space-between;
  align-items: center;
  overflow: hidden;
  padding: 6.4rem 0;
  pointer-events: none;
}

figure:nth-of-type(1) {
  width: 14.4rem;
  height: auto;
  transform: translateX(0rem);
  @include breakpoint(md) {
    transform: translateX(-2rem);
  }
}

figure:nth-of-type(2) {
  display: none;
  width: 20rem;
  height: auto;
  transform: translate(1.2rem, 8rem);
  @include breakpoint(md) {
    display: inherit;
  }
}

figure:nth-of-type(3) {
  width: 21.6rem;
  height: auto;
  transform: translate(1.2rem, -4.8rem);
  @include breakpoint(md) {
    transform: translate(0, -4.8rem);
  }
}

figure:nth-of-type(4) {
  width: 19rem;
  height: auto;
  transform: translateY(2.4rem);
}

figure:nth-of-type(5) {
  display: none;
  width: 17.6rem;
  height: auto;
  transform: translate(1.2rem, 8rem);
  @include breakpoint(md) {
    display: inherit;
  }
}

figure:nth-of-type(6) {
  display: none;
  width: 15.4rem;
  height: auto;
  transform: translate(2.4rem, 1.2rem);
  @include breakpoint(md) {
    display: inherit;
  }
}
</style>

<!-- logic -->
<script>
export default {
  mounted() {
    const random = (min, max) => {
      const delta = max - min;
      return (direction = 1) => (min + delta * Math.random()) * direction;
    };

    const randomX = random(1, 10);
    const randomY = random(1, 10);
    const randomTime = random(3, 5);
    const bubbles = gsap.utils.toArray(".bubble");

    bubbles.forEach((bubble) => {
      gsap.set(bubble, {
        x: randomX(-1),
        y: randomX(1),
      });

      const moveX = (target, direction) => {
        gsap.to(target, randomTime(), {
          x: randomX(direction),
          ease: Sine.easeInOut,
          onComplete: moveX,
          onCompleteParams: [target, direction * -1],
        });
      };

      const moveY = (target, direction) => {
        gsap.to(target, randomTime(), {
          y: randomY(direction),
          ease: Sine.easeInOut,
          onComplete: moveY,
          onCompleteParams: [target, direction * -1],
        });
      };

      moveX(bubble, 1);
      moveY(bubble, -1);
    });
  },
};
</script>
