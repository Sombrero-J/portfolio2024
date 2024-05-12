<script lang="ts">
  import NavButton from "./navButton.svelte";

  let selected = "";

  function handleClick(text: string) {
    selected = text;
    console.log(text);
  }
</script>

<div class="navBar">
  <NavButton
    text="About"
    selected={selected === "About"}
    on:click={() => handleClick("About")}
  />
  <NavButton
    text="Skills"
    selected={selected === "Skills"}
    on:click={() => handleClick("Skills")}
  />
  <NavButton
    text="Awards"
    selected={selected === "Awards"}
    on:click={() => handleClick("Awards")}
  />
  <NavButton
    text="Projects"
    selected={selected === "Projects"}
    on:click={() => handleClick("Projects")}
  />
  <NavButton
    text="Experience"
    selected={selected === "Experience"}
    on:click={() => handleClick("Experience")}
  />
</div>

<style>
    .navBar {
        display: flex;
        justify-content: space-around;
        padding: var(--padding-8) var(--padding-16);
        border-radius: var(--border-radius-md);
        background: hsla(36, 54%, 91%, 0.48);
        box-shadow: var(--shadow-md);
        gap: 1.25rem;
    }
</style>