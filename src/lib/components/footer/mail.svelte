<script>
  import Mail from "$lib/svg/social-media/mail-icon-white.svelte";

  const email = "weng.chan.2@city.ac.uk";
  const subject = "Let's talk!";
  const body = `Hello Weng!`;

  const mailtoLink = `mailto:${email}?subject=${encodeURIComponent(subject)}&body=${encodeURIComponent(body)}`;
</script>

<div class="container">
  <a href={mailtoLink}>weng.chan.2@city.ac.uk</a>
  <Mail />
</div>

<style>
  .container {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: var(--padding-16);
    border-radius: var(--border-radius-lg);
    background-color: var(--color-primary);
    padding: 0.5em 1.5em;
    cursor: pointer;
  }

  a {
    color: var(--color-text-primary-white);
    font-family: var(--font-family-body-primary);
    font-size: var(--font-size-xs);
    font-style: normal;
    font-weight: var(--font-weight-400);
    text-decoration: none;
  }
</style>
