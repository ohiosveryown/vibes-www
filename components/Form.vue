<!-- layout -->
<template>
  <form
    name="contactus"
    action="/thanks"
    method="post"
    netlify
    netlify-honeypot="bot-field"
  >
    <input type="hidden" name="form-name" value="contact" />
    <input
      class="font-sec"
      type="email"
      name="email"
      placeholder="your@email.com"
      required
    />
    <button class="font-sec" type="submit" value="Send message">
      Notify Me
    </button>
  </form>
</template>

<!-- style -->
<style lang="scss" scoped>
@import "~/static/style/grid.scss";
form {
  display: flex;
  flex-direction: row;
  margin: 0 auto 0.8rem;
  width: 100%;
  @include breakpoint(md) {
    margin-bottom: 2.4rem;
    width: 56%;
  }
  @include breakpoint(mdl) {
    width: grid-width(4.25);
  }
}

input,
button {
  margin-bottom: 1.6rem;
  padding: 1.8rem 1rem 2rem;
  font-size: 1.4rem;
  @include breakpoint(md) {
    padding: 1.4rem 2.4rem 1.8rem;
  }
}

input {
  margin-right: 0.8rem;
  padding-left: 2.2rem;
  border-radius: 4px;
  border: 0;
  background: #fff;
  box-shadow: 0px 3px 6px rgba(0, 0, 0, 0.06), 0px 4px 24px rgba(0, 0, 0, 0.06);
  @include breakpoint(md) {
    flex: 1;
    padding-left: 3.2rem;
  }
}

input::placeholder {
  color: var(--gravity);
  opacity: 1;
}

button {
  flex: 1;
  margin-left: 0.2rem;
  border-radius: 4px;
  background: var(--gravity);
  color: #fff;
  transition: all 400ms ease;
  will-change: scale, box-shadow;
  box-shadow: 0 2px 4px #4b4e5a, 0 4px 24px #3c3c46;
  @include breakpoint(md) {
    flex: none;
  }
  &:hover {
    background: 070707;
    transform: scale(1.04);
  }
}
</style>

<!-- logic -->
<script>
export default {};
</script>
