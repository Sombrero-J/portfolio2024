<script>
  import SectionHeading from "./sectionHeading.svelte";
  export let title = "title";
  export let content = "content";
</script>

<div class="card">
  <div class="card__content">{content}</div>
  <SectionHeading heading={title} />
</div>

<style>
  .card {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    width: 50%;
    padding: var(--padding-48);
    border-radius: var(--border-radius-md);
    background: var(--gradient-primary);
    box-shadow: var(--shadow-md);
  }

  .card__content {
    font-family: var(--font-family-body-primary);
    font-size: var(--font-size-xs);
    font-weight: var(--font-weight-4);
    line-height: 1.4;
    color: var(--color-text-primary-black);
  }

  .card__title {
    font-family: var(--font-family-heading-primary);
    font-size: var(--font-size-lg);
    font-weight: var(--font-weight-6);
    line-height: normal;
    color: var(--color-text-primary-black);
  }
</style>
