<script lang="ts">
  import IconsComponent from "./iconsComponent.svelte";

  export let title: string = "default";
</script>

<div class="card">
  <IconsComponent componentName={title} />
  <div class="title">
    {title}
  </div>
</div>

<style>
  .card {
    max-width: 40rem;
    min-width: 30rem;
    min-height: 100%;
    display: flex;
    flex-direction: column;
    align-content: center;
    justify-content: space-between;
    padding: 2rem 2rem;

    border-radius: var(--border-radius-md);
    background: var(--gradient-primary);

    /* card-shadow */
    box-shadow: 0px var(--shadow-md, 4px) var(--shadow-md, 4px) 0px
      rgba(0, 0, 0, 0.25);
    backdrop-filter: blur(17.152769088745117px);
  }

  .title {
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--color-text-accent);
    text-align: center;
    font-family: var(--font-family-heading-secondary);
    font-size: var(--font-size-md);
    font-weight: var(--font-weight-4);
    line-height: 1.6;

    margin-top: 2rem;
    padding: 0em;

    width: 100%;

    border-radius: var(--border-radius-md);
    /* border: 1px solid rgba(255, 255, 255, 0.7); */
    background: linear-gradient(
      264deg,
      rgba(255, 255, 255, 0.4) 14.06%,
      rgba(250, 245, 238, 0.6) 83.01%
    );
    box-shadow: var(--shadow-md);
    backdrop-filter: blur(1.5px);
  }
</style>
