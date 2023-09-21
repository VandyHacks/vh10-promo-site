<script>
  import Tree1 from "../components/sponsors/tree1.svelte";
  import Tree2 from "../components/sponsors/tree2.svelte";
  import Tree3 from "../components/sponsors/tree3.svelte";
  import Building1 from "../components/sponsors/building1.svelte";
  import Building2 from "../components/sponsors/building2.svelte";
  import Sponsor1 from "../components/sponsors/sponsor1.svelte";
  import Sponsor2 from "../components/sponsors/sponsor2.svelte";
</script>

<div class="container">
  <div class="sponsorsHeader">Sponsors</div>

  <div class="comingSoon">Coming Soon</div>

  <div class="sponsor1">
    <!-- TODO: split the title "Sponsors" from our actual sponsor -->
    <!-- <Sponsor1 /> -->
  </div>

  <!-- <div class="sponsor2">
    <Sponsor2 />
  </div> -->

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

<style>
  .container {
    display: block;
    position: relative;
    width: 100vw;
    height: 170vh;
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
    height: 100%;
    margin-top: 30%;
  }
  .comingSoon {
    position: absolute;
    text-shadow: 0 0 7px #fff;
    width: 100%;
    text-align: center;
    color: white;
    font-size: 2em;
    font-weight: 700;
    z-index: 1;
    height: 100%;
    margin-top: 40%;
  }

  .sponsor1 {
    position: absolute;
    width: 40vw;
    left: 30vw;
    top: 30vh;
    z-index: 1;
  }
  /* .sponsor2 {
    position: absolute;
    width: 40vw;
    left: 30vw;
    top: 40vh;
    z-index: 1;
  } */

  .building1 {
    position: absolute;
    width: 25vw;
    top: 60vh;
    right: 1vw;
    z-index: 2;
  }

  .building2 {
    position: absolute;
    width: 25vw;
    top: 110vh;
    z-index: 2;
  }

  .tree1 {
    position: absolute;
    width: 60vw;
    left: -15vw;
    top: 10vh;
    z-index: 3;
  }

  .tree2 {
    position: absolute;
    width: 40vw;
    left: 60vw;
    top: 120vh;
    z-index: 3;
  }

  .tree3 {
    position: absolute;
    width: 20vw;
    left: 80vw;
    top: 2vh;
    z-index: 3;
  }
</style>
