<script>
  import MediaQuery from "../../MediaQuery.svelte";

  import CenterMobile from "./center-mobile.svelte";
  import LeftMobile from "./left-mobile.svelte";
  import RightMobile from "./right-mobile.svelte";
  import DesktopBoard from "./desktop-boards.svelte";

  // TODO: remove this when schedule is ready
  // const SCHEDULE_NOT_READY = true;
</script>

<MediaQuery query="(max-width: 865px)" let:matches>
  {#if matches}
    <div class="all">
      <div class="left-mobile">
        <LeftMobile />
      </div>
      <div class="right-mobile">
        <RightMobile />
      </div>
      <div class="center-mobile">
        <CenterMobile />
      </div>
    </div>
  {:else}
    <DesktopBoard />
  {/if}
</MediaQuery>

<style>
  .all {
    display: grid;
    grid-template-columns: 1fr 1fr;
    justify-content: center;
  }
  .left-mobile {
    width: 50vw;
    left: 0;
  }

  .right-mobile {
    width: 50vw;
    right: 0;
  }
  .center-mobile {
    grid-column: span 2;
    justify-content: center;
  }
</style>
