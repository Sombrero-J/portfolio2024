<script lang="ts">
  export let title: string = "default";
  export let githublink: string = "default";
  export let body: string = "default";

  import JavascriptCircle from "$lib/svg/tech-icon-circle/javascript-circle.svelte";
  import ReactCircle from "$lib/svg/tech-icon-circle/react-circle.svelte";
  import SvelteCircle from "$lib/svg/tech-icon-circle/svelte-circle.svelte";
  import PrismaCircle from "$lib/svg/tech-icon-circle/prisma-circle.svelte";
  import NodeCircle from "$lib/svg/tech-icon-circle/node-circle.svelte";
  import PostgresCircle from "$lib/svg/tech-icon-circle/postgres-circle.svelte";

  import Button from "../button.svelte";

  function handleClick() {
        window.open(githublink, "_blank");
  }
</script>

<div class="container">
  <div class="icon-container">
    <JavascriptCircle />
    <ReactCircle />
    <SvelteCircle />
    <PrismaCircle />
    <NodeCircle />
    <PostgresCircle />
  </div>
  <div class="detail-container">
    <div class="title-bar">
      <div class="title">{title}</div>
      <Button on:click={handleClick} text="GitHub" />
    </div>
    <div class="body">
      {#each body.split("\n") as line}
        <p>{line}</p>
      {/each}
    </div>
  </div>
</div>

<style>
  .container {
    display: flex;
    padding: var(--padding-32);
    background: var(--gradient-primary);
    border-radius: var(--border-radius-md);
    box-shadow: var(--shadow-md);
    width: 40rem;
  }

  .icon-container {
    display: flex;
    flex-wrap: wrap;
    gap: 1rem;
    width: 20%;
  }

  .detail-container {
    width: 80%;
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
  }

  .title-bar {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .title {
    color: var(--color-text-primary-black);
    font-family: var(--font-family-body-primary);
    font-size: var(--font-size-xs);
    font-weight: 600;
  }

  .body {
    color: var(--color-text-primary-black);
    font-family: var(--font-family-body-primary);
    font-size: var(--font-size-xs);
    font-weight: 100;
    line-height: normal;
  }
</style>
