<script>
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

<div class="container">
  <div class="sponsorsHeader">Sponsors</div>

  <!-- Include with asurion page: <div class="glowingArrow"><GlowingArrow /></div> -->

  <div class="sponsorsList">
    <div class="sponsor"><Sponsor1 /></div>
    <div class="sponsor"><Sponsor2 /></div>
    <div class="sponsor"><Sponsor3 /></div>
    <div class="sponsorHorizontal">
      <div class="sponsor"><Sponsor4 /></div>
      <div class="sponsor"><Sponsor10 /></div>
    </div>
    <div class="sponsor"><Sponsor5 /></div>
    <div class="sponsor"><Sponsor6 /></div>
    <div class="sponsor"><Sponsor8 /></div>
    <div class="sponsorHorizontal">
      <div class="sponsor"><Sponsor7 /></div>
      <div class="sponsor"><Sponsor11 /></div>
    </div>
    <div class="sponsor"><Sponsor9 /></div>
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
    z-index: 1;
    margin-top: 50vh;
    width: 30vw;
    left: 35vw;
  }

  .sponsorsList > * {
    z-index: 1;
    width: 30vw;
    margin-top: 5vh;
    stroke: none;
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
    z-index: 3;
  }

  .tree2 {
    position: absolute;
    width: 40vw;
    left: 65vw;
    top: 150vh;
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
