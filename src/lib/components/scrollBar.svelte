<script lang="ts">
  import { onMount } from "svelte";
  import ScrollText from "./scrollText.svelte";

    let scrollerInner: HTMLElement;


  // If a user hasn't opted in for recuded motion, then we add the animation
  onMount(() => {
    if (!window.matchMedia("(prefers-reduced-motion: reduce)").matches) {
        console.log("add animation");
      addAnimation();
    }
  });

  // Function to add animation to scrollers
  function addAnimation() {
    const scrollers = document.querySelectorAll<HTMLElement>(".scroller");

    scrollers.forEach((scroller) => {
      scroller.setAttribute("data-animated", "true");

      const scrollerInner = scroller.querySelector<HTMLElement>(".scroller__inner");
      if (scrollerInner) {
        const scrollerContent = Array.from(scrollerInner.children);

        scrollerContent.forEach((item) => {
          const duplicatedItem = item.cloneNode(true) as HTMLElement;
          duplicatedItem.setAttribute("aria-hidden", "true");
          scrollerInner.appendChild(duplicatedItem);
        });
      }
    });
  }
</script>

<ScrollText text="Software Developer" />

<div class="scroller" data-speed="fast">
    <ul bind:this={scrollerInner} class="tag-list scroller__inner">
    <li>HTML</li>
    <li>CSS</li>
    <li>JS</li>
    <li>SSG</li>
    <li>webdev</li>
    <li>animation</li>
    <li>UI/UX</li>
  </ul>
</div>

<style>
  .scroller {
    max-width: 600px;
  }

  .scroller__inner {
    padding-block: 1rem;
    display: flex;
    flex-wrap: wrap;
    gap: 1rem;
  }

  .scroller[data-animated="true"] {
    overflow: hidden;
    -webkit-mask: linear-gradient(
      90deg,
      transparent,
      white 20%,
      white 80%,
      transparent
    );
    mask: linear-gradient(
      90deg,
      transparent,
      white 20%,
      white 80%,
      transparent
    );
  }

  .scroller[data-animated="true"] .scroller__inner {
    width: max-content;
    flex-wrap: nowrap;
    animation: scroll var(--_animation-duration, 40s)
      var(--_animation-direction, forwards) linear infinite;
  }

  .scroller[data-direction="right"] {
    --_animation-direction: reverse;
  }

  .scroller[data-direction="left"] {
    --_animation-direction: forwards;
  }

  .scroller[data-speed="fast"] {
    --_animation-duration: 20s;
  }

  .scroller[data-speed="slow"] {
    --_animation-duration: 60s;
  }

  @keyframes scroll {
    to {
      transform: translate(calc(-50% - 0.5rem));
    }
  }
</style>
