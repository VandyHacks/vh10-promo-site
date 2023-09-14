<script>
  import MediaQuery from "../../MediaQuery.svelte";
  import BillboardDesktop from "./billboard-desktop.svelte";

  import BillboardMobile from "./billboard-mobile.svelte";
</script>

<MediaQuery query="(max-width: 768px)" let:matches>
  {#if matches}
    <BillboardMobile />
  {:else}
    <BillboardDesktop />
  {/if}
</MediaQuery>
