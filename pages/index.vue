<!-- layout -->
<template>
  <div class="app">
    <Hero
      header="Tidying up the internet so teams and individuals can stay focused."
      subhead="The web is a messy place—it can be overwhelming and disorganized. We believe there's a better way to save, group, and share vibes (oh, and cat videos)."
    />
    
    <!-- Begin Mailchimp Signup Form -->
    <div id="mc_embed_signup">
    <form action="https://pink.us19.list-manage.com/subscribe/post?u=5700e70ce09844674adfea219&amp;id=a7237b2e7b" method="post" id="mc-embedded-subscribe-form" name="mc-embedded-subscribe-form" class="validate" target="_blank" novalidate>
        <div id="mc_embed_signup_scroll">
      
    <div class="mc-field-group">
      <!-- <label for="mce-EMAIL">Email Address </label> -->
      <input type="email" value="" name="EMAIL" class="required email" id="mce-EMAIL">
    </div>
      <div id="mce-responses" class="clear">
        <div class="response" id="mce-error-response" style="display:none"></div>
        <div class="response" id="mce-success-response" style="display:none"></div>
      </div>
        <div style="position: absolute; left: -5000px;" aria-hidden="true"><input type="text" name="b_5700e70ce09844674adfea219_a7237b2e7b" tabindex="-1" value=""></div>
        <div class="clear"><input type="submit" value="Subscribe" name="subscribe" id="mc-embedded-subscribe" class="button"></div>
        </div>
    </form>
    </div>

  </div>
</template>

<!-- style -->
<style lang="scss" scoped>
  @import '~/static/style/grid.scss';

</style>

<!-- logic -->
<script>
  import Hero from '~/components/Hero'
  export default {
    head: () => ({
      title: 'home'
    }),
    components: { Hero, },
    mounted() {

    }
  }
</script>
