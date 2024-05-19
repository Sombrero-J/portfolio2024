<script lang="ts">
  export let text: string = "default";
</script>

<button class="black" on:click>{text}</button>

<style>
  button {
    color: var(--color-text-primary-black);
    font-family: var(--font-family-body-primary);
    font-size: var(--font-size-xxs);
    font-weight: 400;
    cursor: pointer;
  }

  .black {
    padding: var(--padding-3, 0.75rem) var(--padding-5, 1.5rem);
    /* justify-content: center;
    align-items: center;
    gap: 0.5rem; */

    border-radius: var(--border-radius-md);
    border: 2px solid var(--color-primary-dark);
    background: var(--colour-green-100, #cfd8c8);
  }
</style>