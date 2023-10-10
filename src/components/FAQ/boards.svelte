<script>
  import MediaQuery from "../../MediaQuery.svelte";

  import CenterMobile from "./center-mobile.svelte";
  import LeftMobile from "./left-mobile.svelte";
  import RightMobile from "./right-mobile.svelte";
  import CenterDesktop from "./center-desktop.svelte";
  import LeftDesktop from "./left-desktop.svelte";
  import RightDesktop from "./right-desktop.svelte";
</script>

<MediaQuery query="(max-width: 865px)" let:matches>
  {#if matches}
    <div class="all-mobile">
      <div class="left-mobile">
        <LeftMobile />
      </div>
      <div class="center-mobile">
        <CenterMobile />
      </div>
      <div class="right-mobile">
        <RightMobile />
      </div>
    </div>
  {:else}
    <div class="all">
      <div class="left">
        <LeftDesktop />
      </div>
      <div class="center">
        <CenterDesktop />
      </div>
      <div class="right">
        <RightDesktop />
      </div>
    </div>
  {/if}
</MediaQuery>

<style>
  .all {
    display: flex;
    flex-direction: row;
  }
  .left {
    width: 30%;
    left: 0;
    align-items: left;
  }
  .right {
    width: 30%;
    right: 0;
    align-items: right;
  }

  .center {
    width: 40%;
    justify-content: center;
    align-items: center;
  }

  .all-mobile {
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
