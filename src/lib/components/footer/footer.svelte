<script>
  import Mail from "./mail.svelte";
  import CallToAction from "./callToAction.svelte";
  import SocialButton from "./socialButton.svelte";
</script>

<div class="container">
  <CallToAction />
  <Mail />
  <div class="social-section">
    <SocialButton type="behance"/>
    <SocialButton type="linkedin"/>
    <SocialButton type="twitter"/>
    <SocialButton type="github"/>
  </div>
</div>

<style>
  .container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 5rem;
  }

  .social-section {
    display: flex;
    gap: 1rem;
  }
</style>
