<!-- layout -->
<template>
    <nuxt/>
</template>

<!-- style -->
<style lang="scss" scoped>
  @import '~/static/style/grid.scss';
</style>

<!-- logic -->
<script>
  export default {
    mounted() {
      if(('ontouchstart' in window) || (navigator.MaxTouchPoints > 0) || (navigator.msMaxTouchPoints > 0)) {
      } else {
        // smooooth scroll
        document.body.style.height = '100vh'
        Scrollbar.use(OverscrollPlugin)
        Scrollbar.init(document.querySelector('body'), {
          damping: 0.04,
          renderByPixels: true,
          continuousScrolling: true,
          plugins: {
            overscroll: {
              effect: 'bounce',
              damping: .2,
              maxOverscroll: 100,
            }
          }
        })
        // trigger
        let bodyScrollBar = Scrollbar.init(document.querySelector('body'));
        const bdy = document.querySelector('body')
        ScrollTrigger.scrollerProxy(bdy, {
          scrollTop(value) {
            if (arguments.length) {
              bodyScrollBar.scrollTop = value;
            }
            return bodyScrollBar.scrollTop;
          },
          getBoundingClientRect() {
            return {top: 0, left: 0, width: window.innerWidth, height: window.innerHeight};
          }
        })
        bodyScrollBar.addListener(ScrollTrigger.update)
        bodyScrollBar.track.yAxis.element.remove()

        // skew
        const skw = '.skw'
        let proxy = { skew: 0 },
        skewSetter = gsap.quickSetter(skw, "skewY", "deg"),
        clamp = gsap.utils.clamp(-20, 20)

        ScrollTrigger.create({
        scroller: bdy,
        onUpdate: (self) => {
        let skew = clamp(self.getVelocity() / 550);
        if (Math.abs(skew) > Math.abs(proxy.skew)) {
          proxy.skew = skew;
          gsap.to(proxy, {skew: 0, duration: .1, ease: "power4.easeInOut", overwrite: true, onUpdate: () => skewSetter(proxy.skew)})
        }
        }
        })

        gsap.set(skw, {transformOrigin: "center center", force3D: true})
      }
    }
  }
</script>
