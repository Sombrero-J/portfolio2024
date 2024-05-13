<script>
  import Weng from "$lib/components/weng.svelte";
  import NavBar from "$lib/components/navBar.svelte";
  import LongCard from "$lib/components/longCard.svelte";
  import ScrollBar from "$lib/components/scrollBar.svelte";
  import SectionHeading from "$lib/components/sectionHeading.svelte";
  import IconsComponent from "$lib/components/iconsComponent.svelte";
  import IconsShortCard from "$lib/components/iconsShortCard.svelte";
</script>

<div class="hero">
  <Weng />
  <NavBar />
  <LongCard
    title="About"
    content="👋 Hello, World! , I’m Weng Chan, a passionate Web Developer and Graphic Designer on a mission to craft digital experiences that not only look stunning but also function flawlessly.
    With a background in Python, Java, C++, React, and Svelte, I thrive on transforming ideas into interactive realities. Whether it's coding elegant algorithms or designing captivating user interfaces, I'm driven by the challenge of creating seamless, user-centric solutions."
  />
  <ScrollBar />
  <SectionHeading heading="Skills" />

  <div class="skills-container">
    <div class="skills-container__item">
      <IconsShortCard title="Languages" />
    </div>
    <div class="skills-container__item">
      <IconsShortCard title="FrontEnd" />
    </div>
    <div class="skills-container__item"><IconsShortCard title="BackEnd" /></div>
    <div class="skills-container__item tools">
      <IconsShortCard title="ToolsAndSoftware" />
    </div>
  </div>

  <SectionHeading heading="Awards" />
</div>

<style>
  .hero {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    /* height: 100vh; */
    gap: 5rem;
    /* background-color: var(--color-primary); */
    margin: 0 4rem;
  }

  .skills-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-content: center;
    gap: 1.75rem 1rem;
  }

  .skills-container > * {
    flex: 1;
  }

  .tools {
    flex-grow: 0;
    flex-basis: 40%;
  }
</style>
