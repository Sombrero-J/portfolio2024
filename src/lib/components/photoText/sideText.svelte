<script lang="ts">
  export let year: string = "2021";
  export let title: string = "Champion";
  export let event: string = "Microsoft Business Hackathon";
  export let right: boolean = false;
</script>

<div class="sideText" class:right={right}>
  <p class="year">{year}</p>
  <div class="bottom">
    <p class="title">{title}</p>
    <h3 class="event">{event}</h3>
  </div>
</div>

<style>
  .sideText {
    max-width: 10rem;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: flex-start;
    gap: 1rem;
    color: var(--color-text-primary-black);
    flex: 1;
    padding: 1rem 0;
  }

  .right{
    text-align: right;
  }

  .year {
    font-family: "Noto Sans";
    font-size: var(--font-size-xs);
    font-style: normal;
    font-weight: 100;
    line-height: normal;
    width: 100%;
  }

  .title {
    font-family: Anth;
    font-size: var(--font-size-sm);
    font-style: normal;
    font-weight: 400;
  }

  .event {
    font-family: var(--font-family-body-primary);
    font-size: 1.2rem;
    font-style: normal;
    font-weight: var(--font-weight-3);
    line-height: 1;
  }
</style>
