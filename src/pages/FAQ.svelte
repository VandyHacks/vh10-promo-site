<script>
  import Boards from "../components/FAQ/boards.svelte";
</script>

<div>
  <div class="title">FAQ</div>

  <div class="boards">
    <Boards />
  </div>
</div>

<style>
  .title {
    display: flex;
    justify-content: left;
    text-shadow: 0 0 7px #fff;
    color: white;
    font-size: 3em;
    font-weight: 700;
    position: relative;
    /* top: -10em; */
    left: 1em;
    font: Inter;
    z-index: 4;
  }

  .boards {
    width: 100%;
    display: flex;
    justify-content: center;
    position: relative;
    /* top: -45em; */
    z-index: 4;
  }
</style>
