<script>
  import CloudLeft from "../components/schedule/cloud-left.svelte";
  import CloudRight from "../components/schedule/cloud-right.svelte";
  import Billboard from "../components/schedule/billboard.svelte";
  import LightBulb from "../components/schedule/light-bulb.svelte";

  let currentPage = 1;
</script>

<div class="container">
  <!-- cloud -->
  <div class="cloud-left">
    <CloudLeft />
  </div>
  <div class="cloud-right">
    <CloudRight />
  </div>

  <!-- billboard -->
  <div class="center">
    <div class="billboard">
      <Billboard />

      <div class="bulb-container">
        <LightBulb bind:currentPage pageNum="1" />
        <LightBulb bind:currentPage pageNum="2" />
        <LightBulb bind:currentPage pageNum="3" />
      </div>
    </div>
  </div>
</div>

<style>
  .container {
    display: block;
    position: relative;
    width: 100vw;
    height: 100vh;

    /* for development purpose */
    background-color: #140f2e;
    border: 1px solid black;
  }

  .cloud-left {
    position: absolute;
    width: 50vw;
    left: 0px;
    z-index: 1;
  }
  .cloud-right {
    position: absolute;
    width: 10vw;
    right: 0px;
    z-index: 1;
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
  .bulb-container {
    position: absolute;
    width: 30%;
    height: 17%;
    right: 5%;
    top: -12%;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    z-index: -1;

    /* for development purpose */
    /* background-color: greenyellow; */
  }
</style>
