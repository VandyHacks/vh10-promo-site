<script>
  import CloudLeft from "../components/schedule/cloud-left.svelte";
  import CloudRight from "../components/schedule/cloud-right.svelte";
  import Billboard from "../components/schedule/billboard.svelte";
  import LightBulb from "../components/schedule/light-bulb.svelte";
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
      <div class="bulb-1">
        <LightBulb />
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
    background-color: pink;
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

    /* for development purpose */
    background-color: teal;
  }
  .bulb-1 {
    position: absolute;
    top: 0;
    right: 0;
  }

  /* mobile responsiveness */
  @media (max-width: 868px) {
    .billboard {
      width: 95vw;
    }
  }
</style>
