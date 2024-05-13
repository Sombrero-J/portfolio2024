<script lang="ts">
  import Css from "$lib/svg/tech-icon/css.svelte";
  import Cplusplus from "$lib/svg/tech-icon/cplusplus.svelte";
  import Docker from "$lib/svg/tech-icon/docker.svelte";
  import Express from "$lib/svg/tech-icon/express.svelte";
  import Figma from "$lib/svg/tech-icon/figma.svelte";
  import Git from "$lib/svg/tech-icon/git.svelte";
  import Github from "$lib/svg/tech-icon/github.svelte";
  import Github_copilot from "$lib/svg/tech-icon/github_copilot.svelte";
  import Google_cloud from "$lib/svg/tech-icon/google_cloud.svelte";
  import Html5 from "$lib/svg/tech-icon/html5.svelte";
  import Illustrator from "$lib/svg/tech-icon/illustrator.svelte";
  import Intellij from "$lib/svg/tech-icon/intellij.svelte";
  import Java from "$lib/svg/tech-icon/java.svelte";
  import Javascript from "$lib/svg/tech-icon/javascript.svelte";
  import Lightroom from "$lib/svg/tech-icon/lightroom.svelte";
  import Linux from "$lib/svg/tech-icon/linux.svelte";
  import MacOS from "$lib/svg/tech-icon/macOS.svelte";
  import Microsoft from "$lib/svg/tech-icon/microsoft.svelte";
  import Microsoft_teams from "$lib/svg/tech-icon/microsoft_teams.svelte";
  import Mysql from "$lib/svg/tech-icon/mysql.svelte";
  import Nodejs from "$lib/svg/tech-icon/nodejs.svelte";
  import OpenAI from "$lib/svg/tech-icon/openai.svelte";
  import Photoshop from "$lib/svg/tech-icon/photoshop.svelte";
  import Postgres from "$lib/svg/tech-icon/postgres.svelte";
  import Postman from "$lib/svg/tech-icon/postman.svelte";
  import Prisma from "$lib/svg/tech-icon/prisma.svelte";
  import Python from "$lib/svg/tech-icon/python.svelte";
  import React from "$lib/svg/tech-icon/react.svelte";
  import Sass from "$lib/svg/tech-icon/sass.svelte";
  import Svelte from "$lib/svg/tech-icon/svelte.svelte";
  import Typescript from "$lib/svg/tech-icon/typescript.svelte";
  import Vscode from "$lib/svg/tech-icon/vscode.svelte";
  import Xcode from "$lib/svg/tech-icon/xcode.svelte";
  import MicrosoftTeams from "$lib/svg/tech-icon/microsoft_teams.svelte";

  export let componentName: string = "default";

  const toolsAndSoftware = [
    Vscode,
    Intellij,
    Xcode,
    Git,
    Postman,
    Figma,
    Lightroom,
    Illustrator,
    Github,
    Github_copilot,
    Photoshop,
    Linux,
    OpenAI,
    Microsoft_teams,
    Microsoft,
    MacOS,
  ];

  const FrontEnd = [Html5, Css, Javascript, Typescript, Svelte, React, Sass];

  const BackEnd = [
    Nodejs,
    Express,
    Mysql,
    Postgres,
    Prisma,
    Google_cloud,
    Docker,
  ];

  const Languages = [Python, Java, Cplusplus];
  $: selectedComponents = getComponentsArray(componentName.toUpperCase());

  function getComponentsArray(name: string) {
    switch (name) {
      case "TOOLSANDSOFTWARE":
        return toolsAndSoftware;
      case "FRONTEND":
        return FrontEnd;
      case "BACKEND":
        return BackEnd;
      case "LANGUAGES":
        return Languages;
      default:
        return [];
    }
  }
</script>

<div class="icons">
  {#each selectedComponents as Icon}
    <Icon />
  {/each}
</div>

<style>
  .icons {
    /* min-width: 25rem;
    max-width: 35rem; */
    min-height: 60px;
    width: 100%;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-content: center;
    align-content: center;
    gap: 1rem 1.5rem;
  }
</style>