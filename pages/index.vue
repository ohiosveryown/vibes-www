<!-- layout -->
<template>
  <div class="app">
    <Hero
      header="Tidying up the internet so teams and individuals can stay focused."
      subhead="The web is a messy place—it can be overwhelming and disorganized. We believe there's a better way to save, group, and share vibes (oh, and cat videos)."
    />
    <Product />
    <p>
      Lorem ipsum dolor sit, amet consectetur adipisicing elit. Est, eveniet
      possimus ad perferendis earum, at totam esse similique dignissimos
      reprehenderit sunt magnam, omnis ipsa repudiandae expedita! Ducimus quasi
      ab optio! Adipisci harum temporibus autem sunt illo quia illum atque
      expedita, maiores suscipit ea aliquam asperiores voluptates magnam itaque
      sint eveniet nesciunt mollitia ipsa deleniti. Explicabo vel quibusdam
      iusto tempora libero! Ea molestiae, labore esse sapiente quo nisi libero
      ipsam ipsa, doloremque excepturi, magni omnis. Iusto in, quia rem adipisci
      dicta aliquid alias nihil placeat ut voluptatum ipsam officiis suscipit
      nesciunt. Doloribus cupiditate nam repellendus ducimus voluptate nihil,
      aut ratione sint. At non adipisci dolorum quo. Obcaecati voluptas, dolorum
      dignissimos inventore quis, dolore vitae deserunt odio nesciunt sed nam
      sapiente libero? Rem quo minus hic dignissimos! Sint quae tempore autem
      perferendis debitis! Ab labore numquam fuga iusto nesciunt mollitia fugit
      necessitatibus dignissimos ipsum, velit ducimus vel porro fugiat quasi
      provident accusantium?
    </p>
    <p>
      Lorem ipsum dolor sit, amet consectetur adipisicing elit. Est, eveniet
      possimus ad perferendis earum, at totam esse similique dignissimos
      reprehenderit sunt magnam, omnis ipsa repudiandae expedita! Ducimus quasi
      ab optio! Adipisci harum temporibus autem sunt illo quia illum atque
      expedita, maiores suscipit ea aliquam asperiores voluptates magnam itaque
      sint eveniet nesciunt mollitia ipsa deleniti. Explicabo vel quibusdam
      iusto tempora libero! Ea molestiae, labore esse sapiente quo nisi libero
      ipsam ipsa, doloremque excepturi, magni omnis. Iusto in, quia rem adipisci
      dicta aliquid alias nihil placeat ut voluptatum ipsam officiis suscipit
      nesciunt. Doloribus cupiditate nam repellendus ducimus voluptate nihil,
      aut ratione sint. At non adipisci dolorum quo. Obcaecati voluptas, dolorum
      dignissimos inventore quis, dolore vitae deserunt odio nesciunt sed nam
      sapiente libero? Rem quo minus hic dignissimos! Sint quae tempore autem
      perferendis debitis! Ab labore numquam fuga iusto nesciunt mollitia fugit
      necessitatibus dignissimos ipsum, velit ducimus vel porro fugiat quasi
      provident accusantium?
    </p>
  </div>
</template>

<!-- style -->
<style lang="scss" scoped>
@import "~/static/style/grid.scss";
</style>

<!-- logic -->
<script>
import Hero from "~/components/Hero";
import Product from "~/components/Product";
export default {
  head: () => ({
    title: "home",
  }),
  components: { Hero, Product },
  mounted() {},
};
</script>
