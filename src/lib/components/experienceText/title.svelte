<script lang="ts">
  export let title: string = "Default title";
  export let location: string = "Default location";
  export let year: number = -1;

  import PopUp from "./popUp.svelte";

  let active = false;

  function handleMouseEnter() {
    active = true;
  }

  function handleMouseLeave() {
    active = false;
  }
</script>

<div
  class="primary"
  on:mouseenter={handleMouseEnter}
  on:mouseleave={handleMouseLeave}
  role="button"
  tabindex="0"
>
  <h2>{title}</h2>
  <div class="secondary">
    <p>{location}</p>
    <p>{year}</p>
  </div>
  {#if active}
    <div class="pop-up">
      <PopUp {title}/>
    </div>
  {/if}
</div>


<style>
  .pop-up {
    position: absolute;
    bottom: 20px;
    right: 50px;
  }
  h2 {
    color: var(--color-text-primary-black);
    font-family: var(--font-family-body-primary);
    font-size: var(--font-size-xl);
    font-style: normal;
    font-weight: 300;
  }

  p {
    color: var(--color-text-primary-black);
    font-family: var(--font-family-body-primary);
    font-size: var(--font-size-sm);
    font-style: normal;
    font-weight: 100;
    line-height: normal;
  }

  .secondary {
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .primary {
    display: flex;
    flex-direction: column;
    position: relative;
  }
</style>
