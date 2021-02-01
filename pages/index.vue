<!-- layout -->
<template>
  <div class="app">
    <Hero
      header="Tidying up the internet so teams and individuals can stay focused."
      subhead="The web is a messy place—it can be overwhelming and disorganized. We believe there's a better way to save, group, and share vibes (oh, and cat videos)."
    />
    
    <form
    name="contactus"
    action="/"
    method="post"
    netlify
    netlify-honeypot="bot-field">

    <input type="hidden" name="form-name" value="contact"/>
    <div class="name">
      <label class="font-sec" for="name">Your Name</label>
      <input type="text" name="name" required/>
    </div>

    <div class="email">
      <label class="font-sec" for="email">Your Email</label>
      <input type="email" name="email" required/>
    </div>

    <div class="message">
      <label class="font-sec" for="message">Project Information</label>
      <textarea data-autoresize rows="2" name="message" required/>
    </div>

    <button class="font-sec uc" type="submit" value="Send message">Submit Form</button>
  </form>
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
