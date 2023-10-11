<script>
  import MediaQuery from "../MediaQuery.svelte";

  import Tree1 from "../components/sponsors/tree1.svelte";
  import Tree2 from "../components/sponsors/tree2.svelte";
  import Tree3 from "../components/sponsors/tree3.svelte";
  import Building1 from "../components/sponsors/building1.svelte";
  import Building2 from "../components/sponsors/building2.svelte";
  import GlowingArrow from "../components/sponsors/glowingArrow.svelte";
  import Sponsor1 from "../components/sponsors/sponsor1.svelte";
  import Sponsor2 from "../components/sponsors/sponsor2.svelte";
  import Sponsor3 from "../components/sponsors/sponsor3.svelte";
  import Sponsor4 from "../components/sponsors/sponsor4.svelte";
  import Sponsor5 from "../components/sponsors/sponsor5.svelte";
  import Sponsor6 from "../components/sponsors/sponsor6.svelte";
  import Sponsor7 from "../components/sponsors/sponsor7.svelte";
  import Sponsor8 from "../components/sponsors/sponsor8.svelte";
  import Sponsor9 from "../components/sponsors/sponsor9.svelte";
  import Sponsor10 from "../components/sponsors/sponsor10.svelte";
  import Sponsor11 from "../components/sponsors/sponsor11.svelte";
</script>

<MediaQuery query="(max-width: 865px)" let:matches>
  <div class="container">
    <div class="sponsorsHeader">Sponsors</div>

    <div class="sponsorsList" class:sponsorsListMobile={matches}>
      <!-- Asurion -->
      <a class="asurion" href="/asurion" target="_blank">
        <Sponsor1 />
        <div class="glowingArrow">
          <GlowingArrow />
        </div>
      </a>

      <!-- Iron Galaxy Studios -->
      <div>
        <a href="https://www.irongalaxystudios.com/" target="_blank">
          <Sponsor2 />
        </a>
      </div>

      <!-- Google Cloud -->
      <div>
        <a href="https://cloud.google.com/" target="_blank">
          <Sponsor3 />
        </a>
      </div>

      <div class="sponsorHorizontal">
        <!-- Echo 3D -->
        <div>
          <a href="https://www.echo3d.com/" target="_blank">
            <Sponsor4 />
          </a>
        </div>

        <!-- VU ISIS -->
        <div>
          <a href="https://www.isis.vanderbilt.edu/" target="_blank">
            <Sponsor10 /></a
          >
        </div>
      </div>

      <!-- Desmos -->
      <div>
        <a href="https://www.desmos.com/" target="_blank">
          <Sponsor5 />
        </a>
      </div>

      <!-- CareYaya -->
      <div>
        <a href="https://www.careyaya.org/" target="_blank">
          <Sponsor6 />
        </a>
      </div>

      <!-- L3Harris -->
      <div>
        <a href="https://www.l3harris.com/" target="_blank">
          <Sponsor8 />
        </a>
      </div>

      <div class="sponsorHorizontal">
        <!-- Red Bull -->
        <div>
          <a href="https://www.redbull.com/" target="_blank">
            <Sponsor7 />
          </a>
        </div>

        <!-- Patient Safety -->
        <div>
          <a href="https://www.patientsafetytech.com/" target="_blank">
            <Sponsor11 />
          </a>
        </div>
      </div>

      <!-- Qiskit -->
      <div>
        <a href="https://qiskit.org/events/fall-fest" target="_blank">
          <Sponsor9 />
        </a>
      </div>
    </div>

    <div class="building1">
      <Building1 />
    </div>

    <div class="building2">
      <Building2 />
    </div>

    <div class="tree3">
      <Tree3 />
    </div>

    <div class="tree1">
      <Tree1 />
    </div>

    <div class="tree2">
      <Tree2 />
    </div>
  </div>
</MediaQuery>

<style>
  .container {
    display: block;
    position: relative;
    width: 100vw;
    height: 240vh;
  }
  .sponsorsHeader {
    position: absolute;
    text-shadow: 0 0 7px #fff;
    width: 100%;
    text-align: center;
    color: white;
    font-size: 3em;
    font-weight: 700;
    z-index: 1;
    margin-top: 40vh;
  }

  .sponsorsList {
    position: absolute;
    text-align: center;
    z-index: 2;
    margin-top: 50vh;
    width: 30vw;
    left: 35vw;
  }

  .sponsorsList > * {
    z-index: 2;
    width: 30vw;
    margin-top: 5vh;
    stroke: none;
  }

  .sponsorsList:hover > *:not(.sponsorHorizontal),
  .sponsorHorizontal:hover > * {
    cursor: pointer;
  }
  .sponsorsListMobile,
  .sponsorsListMobile > * {
    width: 50vw;
    left: 25vw;
  }

  .sponsorHorizontal {
    display: flex;
  }

  .sponsorHorizontal > * {
    flex: 1;
    height: 100%;
    margin: 5%;
  }

  .building1 {
    position: absolute;
    width: 25vw;
    top: 105vh;
    right: 1vw;
    z-index: 2;
  }

  .building2 {
    position: absolute;
    width: 25vw;
    top: 90vh;
    z-index: 2;
  }

  .tree1 {
    position: absolute;
    width: 60vw;
    left: -15vw;
    top: 10vh;
    z-index: 1;
  }

  .tree2 {
    position: absolute;
    width: 40vw;
    left: 65vw;
    top: 150vh;
    z-index: 1;
  }

  .tree3 {
    position: absolute;
    width: 20vw;
    left: 80vw;
    top: 2vh;
    z-index: 1;
  }
  .asurion {
    width: 30vw;
    height: 100%;
  }
  .asurion:hover {
    cursor: pointer;
  }
  .glowingArrow {
    position: absolute;
    width: 13vw;
    bottom: 95%;
    left: 100%;
  }
</style>
