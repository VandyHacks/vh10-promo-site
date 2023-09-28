<script>
  import MediaQuery from "../MediaQuery.svelte";
  import AboutDesktop from "./About-Desktop.svelte";
  import AboutMobile from "./About-Mobile.svelte";
</script>

<MediaQuery query="(max-width: 1300px)" let:matches>
  {#if matches}
    <AboutMobile />
  {:else}
    <AboutDesktop />
  {/if}
</MediaQuery>
