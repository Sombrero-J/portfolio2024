<script>
  import Behance from "$lib/svg/social-media/behance.svelte";
  import Github from "$lib/svg/social-media/github.svelte";
  import Linkedin from "$lib/svg/social-media/linkedin.svelte";
  import Twitter from "$lib/svg/social-media/twitter.svelte";

  export let type = "behance";
</script>

<div class="container">
  {#if type === "behance"}
    <Behance />
    <a
      href="https://www.behance.net/wengchan"
      target="_blank"
      rel="noopener noreferrer">Behance</a
    >
  {:else if type === "github"}
    <Github />
    <a
      href="https://github.com/Sombrero-J"
      target="_blank"
      rel="noopener noreferrer">GitHub</a
    >
  {:else if type === "linkedin"}
    <Linkedin />
    <a
      href="https://www.linkedin.com/in/wengchan-uk"
      target="_blank"
      rel="noopener noreferrer">LinkedIn</a
    >
  {:else if type === "twitter"}
    <Twitter />
    <a
      href="https://www.behance.net/wengchan"
      target="_blank"
      rel="noopener noreferrer">Twitter</a
    >
  {/if}
</div>

<style>
  .container {
    display: flex;
    padding: 0.75rem 1.5rem;
    align-items: center;
    justify-content: center;
    gap: 1rem;
    border-radius: var(--border-radius-md);
    background: var(--color-black);
  }

  a {
    color: var(--color-text-primary-white);
    font-family: var(--font-family-body-primary);
    font-size: var(--font-size-xxs);
    font-weight: 500;
    line-height: normal;
    text-decoration: none;
  }
</style>
