<script>
    import Weng from '$lib/components/weng.svelte';
    import NavBar from '$lib/components/navBar.svelte';
    import LongCard from '$lib/components/longCard.svelte';
    import ScrollBar from '$lib/components/scrollBar.svelte';
</script>

<div class="hero">
    <Weng />
    <NavBar />
    <LongCard title="About" content="👋 Hello, World! , I’m Weng Chan, a passionate Web Developer and Graphic Designer on a mission to craft digital experiences that not only look stunning but also function flawlessly.
    With a background in Python, Java, C++, React, and Svelte, I thrive on transforming ideas into interactive realities. Whether it's coding elegant algorithms or designing captivating user interfaces, I'm driven by the challenge of creating seamless, user-centric solutions." />
    <ScrollBar />
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
    }
</style>