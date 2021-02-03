<!-- layout -->
<template>
  <section>
    <video
      autoplay="autoplay"
      playsinline=""
      muted
      loop="loop"
      controls="true"
      poster="https://res.cloudinary.com/da32ufmnf/image/upload/v1612194736/vibes-www/cover_snmq67.jpg"
    >
      <source
        src="https://res.cloudinary.com/da32ufmnf/video/upload/v1612283673/vibes-www/v_mfq0fo.mp4"
      />
      <source />
    </video>

    <div class="bubbles">
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

    <div class="bg">
      <img
        class="rainbow"
        src="https://res.cloudinary.com/da32ufmnf/image/upload/v1612318145/vibes-www/bg_fze1pg.jpg"
        alt="document background"
      />
    </div>

    <article class="width">
      <h3 class="mb-2 font-prim">
        Vibes connects your thoughts and ideas all in one&nbsp;place.
      </h3>
      <p class="font-body">
        Save content, create moodboards, organize information, and share ideas
        with&nbsp;others.
      </p>
    </article>
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
  margin: 0 auto 4rem;
  border-radius: 10px;
  max-width: var(--max-width);
  width: 90vw;
  box-shadow: 0px 20px 68px rgba(0, 0, 0, 0.32);
  @include breakpoint(md) {
    margin-bottom: 0;
    width: grid-width(9.5);
  }
}

.bg {
  position: absolute;
  z-index: var(--zmin);
  top: -70rem;
  padding-bottom: 40rem;
  width: 100%;
  opacity: 0.92;
  overflow-x: hidden;
  mix-blend-mode: multiply;
  @include breakpoint(mdl) {
    top: -40rem;
  }
}

.rainbow {
  width: 250vw;
  max-width: none;
  @include breakpoint(md) {
    width: 190vw;
  }
  @include breakpoint(mdl) {
    max-width: 100%;
    width: inherit;
  }
}

.bubbles {
  display: flex;
  justify-content: space-between;
  align-items: center;
  overflow: hidden;
  padding: 6.4rem 0 6.4rem;
  pointer-events: none;
  @include breakpoint(md) {
    padding: 0;
  }
  @include breakpoint(mdl) {
    padding: 4rem 0 6.4rem;
  }
}

figure:nth-of-type(1) {
  width: 14.4rem;
  height: auto;
  transform: translateX(-2rem);
}

figure:nth-of-type(2) {
  display: none;
  width: 20rem;
  height: auto;
  transform: translate(1.2rem, 8rem);
  @include breakpoint(md) {
    display: inherit;
    transform: translate(0rem, 4rem);
  }
  @include breakpoint(mdl) {
    transform: translate(1.2rem, 8rem);
  }
}

figure:nth-of-type(3) {
  width: 21.6rem;
  height: auto;
  transform: translateY(-2.4rem);
  @include breakpoint(md) {
    transform: translateY(-1.2rem);
  }
  @include breakpoint(mdl) {
    transform: translateY(-4.8rem);
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
    transform: translate(1.2rem, 4rem);
  }
  @include breakpoint(mdl) {
    transform: translate(1.2rem, 8rem);
  }
}

figure:nth-of-type(6) {
  width: 15.4rem;
  height: auto;
  transform: translateX(1.2rem);
  @include breakpoint(md) {
    transform: translate(2.4rem, 1.2rem);
  }
}

article {
  margin: 0 auto;
  padding-bottom: 4rem;
  text-align: center;
  @include breakpoint(md) {
    padding-bottom: 7.2rem;
    width: grid-width(8);
  }
  @include breakpoint(mdl) {
    width: grid-width(6);
  }
}

h3 {
  font-size: 2.8rem;
  line-height: 1.2;
  @include breakpoint(md) {
    font-size: 4rem;
  }
}
p {
  font-size: 1.6rem;
  @include breakpoint(md) {
    font-size: 2rem;
  }
}
</style>

<!-- logic -->
<script>
import Rainbow from "./Rainbow";
export default {
  components: { Rainbow },
  mounted() {
    const getBubbles = document.querySelector(".bubbles");
    if (navigator.userAgent.indexOf("Chrome") > 0) {
      const mq = matchMedia("(min-width: 700px)");
      if (mq.matches) {
        getBubbles.style.padding = "16rem 0";
      } else {
        getBubbles.style.padding = "6.4rem 0 8rem";
      }
      console.log("Chrome");
    } else {
      console.log("Not Chrome");
    }
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
