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

  <!-- Billboard -->
  <div class="container">
    <div class="title" class:title-mobile={matches}>Schedule</div>

    <div class="content">
      {#if currentPage == 1}
        <!-- TODO: render page 1 content here -->
        {#each page1Data.events as event}
          {@const eventName = event.name}
          {@const eventTime = event.time}
          <div class="row">
            <div class="row-start">
              {#each eventName as char}
                <span class="row-item">{char}</span>
              {/each}
            </div>
            <div class="row-end">
              {#each eventTime as char}
                <span class="row-item">{char}</span>
              {/each}
            </div>
          </div>
        {/each}
      {:else if currentPage == 2}
        <!-- TODO: render page 2 content here -->
        {#each page2Data.events as event}
          {@const eventName = event.name}
          {@const eventTime = event.time}
          <div class="row">
            <div class="row-start">
              {#each eventName as char}
                <span class="row-item">{char}</span>
              {/each}
            </div>
            <div class="row-end">
              {#each eventTime as char}
                <span class="row-item">{char}</span>
              {/each}
            </div>
          </div>
        {/each}
      {/if}
    </div>
  </div>

  <!-- light bulbs -->
  <div class="bulb-container" class:bulb-container-mobile={matches}>
    <LightBulb bind:currentPage pageNum="1" date={page1Data.date} />
    <LightBulb bind:currentPage pageNum="2" date={page2Data.date} />
  </div>
</MediaQuery>

<style>
  /* Container */
  .container {
    position: absolute;
    width: 90%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  /* Title */
  .title {
    font-size: 3rem;
    font-weight: 500;
  }

  .title-mobile {
    font-size: 2rem;
    top: 13%;
  }

  /* Schedule content and monospace rows */
  .content {
    width: 100%;
  }
  .row {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    width: 100%;
    margin: 0.5rem 0;
    font-family: monospace;
    font-size: x-large;
  }
  .row-item {
    margin: 0 1px;
    padding: 0 2px;
    border: 0.01em solid rgb(211, 211, 211);
    background-color: white;
  }

  /* Lightbulb container */
  .bulb-container {
    position: absolute;
    width: 20%;
    height: 17%;
    right: 5%;
    top: -12%;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
  }
  .bulb-container-mobile {
    width: 40%;
    height: 17%;
    right: auto;
    top: -8%;
  }
</style>
