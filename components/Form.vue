<!-- layout -->
<template>
  <form
    name="contactus"
    action="/"
    method="post"
    netlify
    netlify-honeypot="bot-field">
    <input 
      type="hidden" 
      name="form-name" 
      value="contact"
    />
    <input 
      class="font-sec"
      type="email" 
      name="email" 
      placeholder="your@email.com"
      required
    />
    <button 
      class="font-sec"
      type="submit" 
      value="Send message">
      Notify Me
    </button>
  </form>
</template>

<!-- style -->
<style lang="scss" scoped>
  @import '~/static/style/grid.scss';
  form {
    display: flex;
    width: 100%;
    @include breakpoint(sm) { width: 38.6rem; }
  }
  
  input, button {
    padding: 1.4rem 2.4rem 1.8rem;
    font-size: 1.4rem;
  }
  
  input {
    flex: 1;
    margin-right: .8rem;
    border-radius: 4px;
    border: 0;
    background: #fff;
    box-shadow: 
      0px 3px 6px rgba(0, 0, 0, 0.06), 
      0px 4px 24px rgba(0, 0, 0, 0.06);
  }
  
  input::placeholder { 
    color: var(--gravity); 
    opacity: 1;
  }
  
  button {
    margin-left: .2rem;
    border-radius: 4px;
    background: var(--gravity);
    color: #fff;
    box-shadow: 
      0px 2px 4px rgba(0, 0, 0, 0.12), 
      0px 4px 25px rgba(0, 0, 0, 0.25);
  }
</style>

<!-- logic -->
<script>
  export default {

  }
</script>