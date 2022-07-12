<script>
  import Project from "./Project.svelte";
  let projects = Array(13).fill("Hello there");
</script>

<div class="flex pt-10 mb-10 gap-10 flex-wrap justify-evenly">
  {#each projects as proj}
    <Project src={proj} />
  {/each}
</div>
