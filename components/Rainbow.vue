<!-- layout -->
<template>
  <div class="rainbow-wrapper">
    <svg
      class="layer-0"
      width="100%"
      height="1294"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
    >
      <path
        d="M1699 740.298L-116 1294C-116 317.261 587.747-18.667 998.498.793 1327.1 16.362 1602.42 500.283 1699 740.298z"
        fill="url(#paint0_linear)"
      />
      <defs>
        <linearGradient
          id="paint0_linear"
          x1="-89.111"
          y1="1294.46"
          x2="791.14"
          y2="179.642"
          gradientUnits="userSpaceOnUse"
        >
          <stop stop-color="#964EB7" />
          <stop offset=".432" stop-color="#F090BD" />
          <stop offset="1" stop-color="#D8C8FA" />
        </linearGradient>
      </defs>
    </svg>

    <svg
      class="layer-1"
      width="100%"
      height="893"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
    >
      <path
        d="M849.5 8.997c-345.6-86.8-739 493.5-892.5 794.5 509.333 71.666 1527.5 168.1 1525.5-19.5-2.5-234.5-201-666.5-633-775z"
        fill="url(#paint1_linear)"
      />
      <defs>
        <linearGradient
          id="paint1_linear"
          x1="719.751"
          y1="893"
          x2="719.751"
          y2=".246"
          gradientUnits="userSpaceOnUse"
        >
          <stop stop-color="#413DAE" />
          <stop offset="1" stop-color="#7076CF" />
        </linearGradient>
      </defs>
    </svg>

    <svg
      class="layer-2"
      width="1440"
      height="316"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
    >
      <path
        d="M974 0c177.39 0 286.8 71.215 349.58 134.952 35.06 35.604 80.45 61.892 130.42 61.892V316H-1V100.784c113.5 0 165 117.057 404.5 117.057S733.2 0 974 0z"
        fill="url(#paint2_linear)"
      />
      <defs>
        <linearGradient
          id="paint2_linear"
          x1="1454"
          y1="19.75"
          x2="747.474"
          y2="910.005"
          gradientUnits="userSpaceOnUse"
        >
          <stop stop-color="#F0449F" />
          <stop offset="1" stop-color="#F7A080" />
        </linearGradient>
      </defs>
    </svg>

    <svg
      class="layer-3"
      width="437"
      height="319"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
    >
      <path
        d="M436.942 312.386c-140.666 17-424.9 11.7-436.5-145.5-14.5-196.5 331.5-294 436.5 145.5z"
        fill="url(#paint0_linear)"
      />
      <defs>
        <linearGradient
          id="paint3_linear"
          x1="218.471"
          y1="319"
          x2="218.471"
          y2=".793"
          gradientUnits="userSpaceOnUse"
        >
          <stop stop-color="#F0C7DA" />
          <stop offset="1" stop-color="#EF7ECF" />
        </linearGradient>
      </defs>
    </svg>
  </div>
</template>

<!-- style -->
<style lang="scss" scoped>
@import "~/static/style/grid.scss";
.rainbow-wrapper {
  position: relative;
  width: 100%;
  top: 20rem;
  opacity: 0.72;
}

.layer-0 {
}

.layer-1 {
  position: absolute;
  top: 24rem;
}

.layer-2 {
  position: absolute;
  top: 48rem;
}

.layer-3 {
  position: absolute;
  top: 17rem;
  right: 6.4rem;
}
</style>

<!-- logic -->
<script>
export default {
  mounted() {},
};
</script>
