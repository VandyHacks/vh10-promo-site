<script>
  import MediaQuery from "../../MediaQuery.svelte";
  import schedule from "../../data/schedule.json";

  import BillboardDesktop from "./billboard-desktop.svelte";
  import BillboardMobile from "./billboard-mobile.svelte";
  import LightBulb from "./light-bulb.svelte";

  export let currentPage;

  let page1Data = schedule[0];
  let page2Data = schedule[1];
</script>

<MediaQuery query="(max-width: 768px)" let:matches>
  {#if matches}
    <BillboardMobile />
  {:else}
    <BillboardDesktop />
  {/if}

  <div class="container">
    <div class="title" class:title-mobile={matches}>Schedule</div>
    {#if currentPage == 1}
      <!-- TODO: render page 1 content here -->
      {#each page1Data.events as event}
        <div>{event.name} | {event.time}</div>
      {/each}
    {:else if currentPage == 2}
      <!-- TODO: render page 2 content here -->
      {#each page2Data.events as event}
        <div>{event.name} | {event.time}</div>
      {/each}
    {/if}
  </div>

  <!-- light bulbs -->
  <div class="bulb-container" class:bulb-container-mobile={matches}>
    <LightBulb bind:currentPage pageNum="1" />
    <LightBulb bind:currentPage pageNum="2" />
  </div>
</MediaQuery>

<style>
  .container {
    position: absolute;
    width: 90%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
  }

  .title {
    font-size: 3rem;
    font-weight: 500;
    margin-bottom: 2rem;
    position: absolute;
    top: 10%;
  }

  .title-mobile {
    font-size: 2rem;
    top: 13%;
  }

  .bulb-container {
    position: absolute;
    width: 20%;
    height: 17%;
    right: 5%;
    top: -12%;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    z-index: -1;
  }
  .bulb-container-mobile {
    width: 40%;
    height: 17%;
    right: auto;
    top: -8%;
  }
</style>
