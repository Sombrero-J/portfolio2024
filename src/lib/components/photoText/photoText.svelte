<script lang="ts">
  import SideText from "./sideText.svelte";
  export let image: string = "default";
  export let left: boolean = false;
</script>

<div class="container">
  {#if left}
    <SideText right={true} />
  {/if}
  {#if image === "london42"}
    <enhanced:img
      src="$lib/assets/london42.png"
      alt="london42 hackathon"
      class="img"
    />
  {:else if image === "microsoftbusiness"}
    <enhanced:img
      src="$lib/assets/microsoftbusiness.png"
      alt="microsoft business hackathon"
      class="img"
    />
  {:else if image === "microsoftregional"}
    <enhanced:img
      src="$lib/assets/microsoftregional.png"
      alt="microsoft regional hackathon"
      class="img"
    />
  {:else if image === "tezos"}
    <enhanced:img
      src="$lib/assets/tezos.png"
      alt="tezos hackathon"
      class="img"
    />
  {/if}
  {#if !left}
    <SideText right={false} />
  {/if}
</div>

<style>
  .container {
    display: flex;
    justify-content: center;
    /* align-items: stretch; */
    gap: 1rem;
    color: var(--color-text-primary-black);
    /* flex: 1; */
  }

  .img {
    width: 14rem;
    height: auto;
  }
</style>
