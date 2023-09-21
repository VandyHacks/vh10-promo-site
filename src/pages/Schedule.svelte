<script>
  import MediaQuery from "../MediaQuery.svelte";

  import MountainLeft from "../components/schedule/mountain-left.svelte";
  import MountainRight from "../components/schedule/mountain-right.svelte";
  import Billboard from "../components/schedule/billboard.svelte";
  import BuildingLeft from "../components/schedule/building-left.svelte";
  import BuildingRight from "../components/schedule/building-right.svelte";
  import BuildingBottom from "../components/schedule/building-bottom.svelte";
  import BuildingTop from "../components/schedule/building-top.svelte";
  import RoadTop from "../components/schedule/road-top.svelte";
  import MountainMobile from "../components/schedule/mountain-mobile.svelte";

  let currentPage = 1;
</script>

<MediaQuery query="(max-width: 768px)" let:matches>
  <div class="container">
    {#if !matches}
      <!-- desktop background -->
      <div class="mountain-left">
        <MountainLeft />
      </div>
      <div class="mountain-right">
        <MountainRight />
      </div>
      <div class="road-top">
        <RoadTop />
      </div>
      <div class="building-left">
        <BuildingLeft />
      </div>
      <div class="building-right">
        <BuildingRight />
      </div>
      <div class="building-bottom">
        <BuildingBottom />
      </div>
      <div class="building-top">
        <BuildingTop />
      </div>
    {:else}
      <!-- mobile background -->
      <div class="mountain-mobile">
        <MountainMobile />
      </div>
    {/if}

    <!-- billboard -->
    <div class="center">
      <div class="billboard">
        <Billboard bind:currentPage />
      </div>
    </div>
  </div>
</MediaQuery>

<style>
  .container {
    display: block;
    position: relative;
    width: 100vw;
    height: 100vh;
  }
  .center {
    position: absolute;
    width: 100vw;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 2;
  }
  .billboard {
    position: relative;
    margin: 0 auto;
    display: flex;
    width: 900px;
    height: 600px;
    object-fit: fill;
    justify-content: center;

    /* for development purpose */
    /* background-color: teal; */
  }
  .road-top {
    position: absolute;
    width: 110vw;
    bottom: 0px;
    height: 79vh;
    z-index: 1;
    left: -5vw;
  }
  .mountain-left {
    position: absolute;
    width: 50vw;
    left: 0px;
    z-index: 1;
  }
  .mountain-right {
    position: absolute;
    width: 10vw;
    right: 0px;
    z-index: 1;
  }
  .mountain-mobile {
    position: absolute;
    width: 100vw;
  }
  .building-left {
    position: absolute;
    width: 15vw;
    left: 0px;
    top: 25vh;
    z-index: 2;
  }
  .building-right {
    position: absolute;
    width: 50vw;
    right: 0px;
    top: 25vh;
    z-index: 2;
  }
  .building-bottom {
    position: absolute;
    width: 100vw;
    bottom: -10vh;
    z-index: 1;
    right: 3;
  }
  .building-top {
    position: absolute;
    width: 90vw;
    left: 50%;
    top: 50%;
    transform: translateX(-45%) translateY(-40%);
    z-index: 1;
  }
</style>
