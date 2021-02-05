<!-- layout -->
<template>
  <div class="app">
    <header>
      <div class="bubbles enter">
        <figure>
          <img
            class="bubble bubble-01"
            src="../static/img/bubble-01.png"
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

      <h1 class="width enter font-prim">
        Good vibes will be coming your way soon.
      </h1>
      <h2 class="width enter">
        Thanks for signing up. You'll be the first to know when Vibes has been
        opened up for use ✨🔮.
      </h2>
      <Icon class="icon enter" />
      <h3 class="font-sec enter">
        <a
          target="_blank"
          href="https://twitter.com/cmykw_/status/1196273185987211264"
          >Follow Updates on Twitter</a
        >
      </h3>
    </header>
    <img
      src="https://res.cloudinary.com/da32ufmnf/image/upload/v1612319533/vibes-www/bg-footer_mbxpa9.jpg"
      alt=""
      class="bg rainbow-enter"
    />
  </div>
</template>

<!-- style -->
<style lang="scss" scoped>
@import "~/static/style/grid.scss";
header {
  display: flex;
  flex-direction: column;
  align-items: center;
  position: relative;
  margin: 0 auto;
  min-height: 100vh;
  overflow-x: hidden;
  @include breakpoint(md) {
    margin-bottom: 4.8rem;
  }

  @include breakpoint(mdl) {
    margin-bottom: 2.4rem;
  }
}

h1,
h2 {
  text-align: center;
}
h1 {
  margin: 14rem 0 1.2rem;
  font-size: 3.6rem;
  line-height: 1;
  @include breakpoint(md) {
    margin: 18rem 0 2rem;
    width: grid-width(10);
    font-size: 8.8vw;
  }
  @include breakpoint(mdl) {
    margin: 18rem 0 4rem;
    width: grid-width(8);
    font-size: 7.2vw;
  }
}
h2 {
  margin-top: 1.2rem;
  margin: 1.2rem 0 4.8rem;
  font-size: 1.9rem;
  @include breakpoint(md) {
    margin: 0 0 4.8rem;
    max-width: 56ch;
    width: grid-width(8);
    font-size: 2rem;
  }
  @include breakpoint(mdl) {
    margin: 0 0 6.4rem;
    width: grid-width(5.5);
  }
}

h3 {
  margin-top: 4rem;
  font-size: 1.4rem;
  @include breakpoint(md) {
    margin-top: 6.4rem;
  }
}

.bubbles {
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: absolute;
  z-index: var(--zmin);
  top: 0;
  left: 0;
  width: 100%;
  pointer-events: none;
  @include breakpoint(md) {
    top: -20rem;
  }
}

figure:nth-of-type(1) {
  width: 20rem;
  height: auto;
  transform: translateX(-0.8rem);
  @include breakpoint(md) {
    width: 14.4rem;
  }
  @include breakpoint(mdl) {
    width: 18rem;
    transform: translate(-2rem, 4.2rem);
  }
}

figure:nth-of-type(2) {
  display: none;
  width: 20rem;
  height: auto;
  transform: translate(1.2rem, 8rem);
  @include breakpoint(md) {
    display: inherit;
    transform: translate(0, 4rem);
  }
  @include breakpoint(mdl) {
    width: 24rem;
    transform: translateX(1.2rem);
  }
}

figure:nth-of-type(3) {
  width: 24rem;
  height: auto;
  transform: translateY(-2.4rem);
  @include breakpoint(md) {
    width: 21.6rem;
    transform: translateY(-1.2rem);
  }
  @include breakpoint(mdl) {
    width: 26rem;
    transform: translateY(-4.8rem);
  }
}

figure:nth-of-type(4) {
  width: 24rem;
  height: auto;
  transform: translateY(2.4rem);
  @include breakpoint(md) {
    width: 19rem;
  }
}

figure:nth-of-type(5) {
  display: none;
  width: 17.6rem;
  height: auto;
  transform: translate(1.2rem, 8rem);
  @include breakpoint(md) {
    display: inherit;
    transform: translate(1.2rem, 4rem);
  }
  @include breakpoint(mdl) {
    width: 22rem;
  }
}

figure:nth-of-type(6) {
  width: 18rem;
  height: auto;
  transform: translateX(0.2rem);
  @include breakpoint(md) {
    width: 18rem;
    transform: translate(2.4rem, 1.2rem);
  }
}

.bg {
  position: absolute;
  z-index: var(--zmin);
  bottom: -6.4rem;
  width: 100vw;
  mix-blend-mode: multiply;
  @include breakpoint(md) {
    bottom: -11.2rem;
  }
}
</style>

<!-- logic -->
<script>
import Icon from "~/components/Icon";
export default {
  head: () => ({
    title: "V I B E S ✨",
  }),
  components: { Icon },
  mounted() {
    gsap.from(".enter", {
      opacity: 0,
      y: 200,
      stagger: 0.075,
      duration: 1,
      delay: 1,
      ease: Power2.easeInOut,
    });

    gsap.from(".rainbow-enter", {
      opacity: 0,
      duration: 1,
      delay: 1,
      ease: Power2.easeInOut,
    });

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
