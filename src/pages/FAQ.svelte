<script>
  import Boards from "../components/FAQ/boards.svelte";
  import CenterMobile from "../components/FAQ/center-mobile.svelte";
  import LeftMobile from "../components/FAQ/left-mobile.svelte";
  import RightMobile from "../components/FAQ/right-mobile.svelte";
  import DesktopBoards from "../components/FAQ/desktop-boards.svelte";
</script>

<div class="container">
  <div class="title">FAQ</div>
  <div class="boards">
    <Boards />
  </div>
</div>

<style>
  .container {
    display: block;
    position: relative;
    width: 100vw;
    height: 100vh;
  }
  .title {
    display: flex;
    justify-content: center;
    align-items: center;
    text-shadow: 0 0 7px #fff;
    color: white;
    width: 30vw;
    padding-left: 10px;
    padding-top: 5vh;
    font-size: 3em;
    font-weight: 700;
  }
  .boards {
    width: 100%;
    height: 90%;
    display: flex;
    justify-content: center;
    align-items: center;
  }
</style>
