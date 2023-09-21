<script>
  import Billboard from "../components/schedule/billboard.svelte";
  import LightBulb from "../components/schedule/light-bulb.svelte";
  import Scene from "../components/schedule/scene.svelte";

  let currentPage = 1;
</script>

<div class="container">
  <div class="scene" style="position:absolute;">
    <Scene />
  </div>

  <!-- billboard -->
  <div class="center">
    <div class="billboard">
      <Billboard />

      <div class="bulb-container">
        <LightBulb bind:currentPage pageNum="1" />
        <LightBulb bind:currentPage pageNum="2" />
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
    margin-bottom: 20em;

    /* for development purpose */
    background-color: #140f2e;
    border: 1px solid black;
  }

  .center {
    position: absolute;
    width: 100vw;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 4;
  }
  .billboard {
    position: relative;
    margin: 0 auto;
    display: flex;
    width: 90vw;
    height: 600px;
    object-fit: fill;
    justify-content: center;

    /* for development purpose */
    /* background-color: teal; */
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
    z-index: 3;

    /* for development purpose */
    /* background-color: greenyellow; */
  }

  .scene {
    width: 100%;
    z-index: 2;
    position: absolute;
    top: -15em;
  }

  @media (max-width: 450px) {
    .scene {
      display: none;
    }
  }
</style>
