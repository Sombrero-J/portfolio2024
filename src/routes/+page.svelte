<script>
  import Weng from "$lib/components/weng.svelte";
  import NavBar from "$lib/components/navBar.svelte";
  import LongCard from "$lib/components/longCard.svelte";
  import ScrollBar from "$lib/components/scrollBar.svelte";
  import SectionHeading from "$lib/components/sectionHeading.svelte";
  import IconsShortCard from "$lib/components/iconsShortCard.svelte";
  import PhotoText from "$lib/components/photoText/photoText.svelte";
  import ProjectCard from "$lib/components/projectCard/projectCard.svelte";
  import Title from "$lib/components/experienceText/title.svelte";
  import Footer from "$lib/components/footer/footer.svelte";
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
  <div class="awards-container">
    <div class="awards-container__left">
      <div class="cushion"></div>
      <PhotoText left={true} image="microsoftregional" />
      <PhotoText left={true} image="microsoftbusiness" />
    </div>
    <div class="awards-container__right">
      <PhotoText left={false} image="tezos" />
      <PhotoText left={false} image="london42" />
    </div>
  </div>

  <SectionHeading heading="Projects" />
  <div class="project-section">
    <ProjectCard
      title="TruthChain"
      githublink="https://github.com/Sombrero-J/portfolio2024"
      body={`Decentralised Blockchain Application \n Validating Information through Stake Voting \n Svelte - SmartPy - Prisma`}
    />
    <ProjectCard
      title="Exe.Learn.AI"
      githublink="https://github.com/Sombrero-J/portfolio2024"
      body={`Decentralised Blockchain Application \n Validating Information through Stake Voting \n Svelte - SmartPy - Prisma`}
    />
    <ProjectCard
      title="Principle.AI"
      githublink="https://github.com/Sombrero-J/portfolio2024"
      body={`Decentralised Blockchain Application \n Validating Information through Stake Voting \n Svelte - SmartPy - Prisma`}
    />
    <ProjectCard
      title="2D Interactive Shooting Game"
      githublink="https://github.com/Sombrero-J/portfolio2024"
      body={`Decentralised Blockchain Application \n Validating Information through Stake Voting \n Svelte - SmartPy - Prisma`}
    />
  </div>

  <SectionHeading heading="Experience" />
  <Title title="Student Representative" location="City, Uni" year={2024} />
  <Title title="Course Ambassador" location="City, Uni" year={2023} />
  <Footer />
</div>

<style>
  .project-section {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    width: 70%;
    gap: 1rem;
  }
  .awards-container__right {
    display: flex;
    flex-direction: column;
    gap: 3rem;
  }
  .awards-container__left {
    display: flex;
    flex-direction: column;
    gap: 3rem;
  }
  .cushion {
    height: 5rem;
  }
  .awards-container {
    display: flex;
    justify-content: center;
    gap: 1rem;
  }

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
