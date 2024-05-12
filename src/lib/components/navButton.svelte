<script>
  import { createEventDispatcher } from "svelte";
  export let text = "default";
  export let selected = false;
  const dispatch = createEventDispatcher();
</script>

<a href={`#{text}`} class="navButton" class:selected on:click>{text}</a>

<style>
  .navButton {
    padding: var(--padding-3) var(--padding-8);
    border-radius: var(--border-radius-md);
    font-family: var(--font-family-heading-primary);
    color: var(--color-text-primary-black);
    text-decoration: none;
    font-size: var(--font-size-lg, 3rem);
    font-weight: 600;
    line-height: normal;
  }

  .selected {
    background: var(--color-primary);
    color: var(--color-text-primary-white);
  }

  .navButton:hover:not(.selected) {
    background: var(--color-secondary);
    color: var(--color-text-primary-black);
  }
</style>
