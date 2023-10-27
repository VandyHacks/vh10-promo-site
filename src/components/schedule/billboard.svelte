<script>
  import MediaQuery from "../../MediaQuery.svelte";
  import schedule from "../../data/schedule.json";

  import BillboardDesktop from "./billboard-desktop.svelte";
  import BillboardMobile from "./billboard-mobile.svelte";
  import LightBulb from "./light-bulb.svelte";

  export let currentPage;

  let page1Data = schedule[0];
  let page2Data = schedule[1];

  // TODO: remove this when schedule is ready
  const SCHEDULE_NOT_READY = false;
</script>

<MediaQuery query="(max-width: 768px)" let:matches>
  {#if matches}
    <BillboardMobile />
  {:else}
    <BillboardDesktop />
  {/if}

  <!-- Billboard -->
  <div class="container" class:container-mobile={matches}>
    <div class="title" class:title-mobile={matches}>Schedule</div>

    <div class="content" class:content-mobile={matches}>
      {#if SCHEDULE_NOT_READY}
        <div class="coming-soon">COMING SOON</div>
      {:else if currentPage == 1}
        <!-- TODO: render page 1 content here -->
        {#each page1Data.events as event}
          {@const eventName = event.name}
          {@const eventTime = event.time}
          <div class:row={!matches} class:row-mobile={matches}>
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
          <div class:row={!matches} class:row-mobile={matches}>
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
    height: 80%;
    display: flex;
    flex-direction: column;
    align-self: center;
    align-items: center;
  }
  .container-mobile {
    width: 290px;
    /* background-color: red; */
  }

  /* Title */
  .title {
    font-size: 3rem;
    font-weight: 500;
    padding-bottom: 2%;
  }

  .title-mobile {
    font-size: 2rem;
    top: 13%;
  }

  /* Schedule content and monospace rows */
  .content {
    width: 100%;
    overflow-y: scroll;
    font-family: Inter;
    font-size: x-large;
  }
  .content-mobile {
    font-size: small;
    font-family: Inter;
  }
  .row {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    width: 100%;
    margin: 0.5rem 0;
    border-bottom: 0.01em solid rgb(211, 211, 211);
  }
  .row-mobile {
    margin: 0.5rem 0;
    border-bottom: 0.01em solid rgb(211, 211, 211);
  }
  .row-item {
    margin: 0 0.25px;
    /* padding: 0 2px; */
    /* border: 0.01em solid rgb(211, 211, 211); */
    /* background-color: white; */
  }
  .row-end {
    margin-left: 5%;
    white-space: nowrap;
    text-align: right;
    /* background-color: white; */
  }

  /* Lightbulb container */
  .bulb-container {
    position: absolute;
    width: 20%;
    /* height: 17%; */
    right: 5%;
    top: -12%;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
  }
  .bulb-container-mobile {
    position: absolute;
    width: 30%;
    /* height: 17%; */
    right: auto;
    top: -6vh;
    /* background-color: white; */
  }
  .coming-soon {
    font-size: 3rem;
    font-weight: 500;
    color: rgb(211, 211, 211);
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
  }
</style>
