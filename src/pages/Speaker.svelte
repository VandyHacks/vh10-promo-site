<script>
  import SpeakerCircle from "../components/speaker/speakerCircle.svelte";
  import Scene from "../components/speaker/scene.svelte";
</script>

<div style="position:relative;">
  <div class="speakerAndText" style="position:absolute;">
    <div class="speakercircle">
      <SpeakerCircle />
    </div>

    <div class="text">
      <div class="title">Speaker Series</div>
      <div class="name">Co-President Alex Oh</div>
      <div class="description">
        Alex Oh is a junior at Vanderbilt University and is a really cool dude.
        Like a really cool dude. He is also one of the Co-Presidents of
        VandyHacks X. This is another sentence talking about how awesome he is.
      </div>
      <!-- implement logic for changing names and description -->
    </div>
  </div>

  <div class="scene" style="position:absolute;">
    <Scene />
  </div>
</div>

<style>
  .speakercircle {
    width: 40%;
    float: left;
    padding-left: 7vw;
    z-index: 4;
    position: relative;
    top: -15em;
  }
  .text {
    width: 40%;
    float: right;
    font: Inter;
    font-size: 1.5em;
    font-weight: 200;
    padding-right: 7vw;
    z-index: 4;
  }
  .title {
    display: flex;
    justify-content: left;
    text-shadow: 0 0 7px #fff;
    color: white;
    font-size: 3em;
    font-weight: 700;
    position: relative;
    top: -2em;
    font: Inter;
    z-index: 4;
  }

  .name {
    display: flex;
    justify-content: left;
    font-size: 1.4em;
    font-weight: 700;
    position: relative;
    top: -3em;
    color: white;
    font: Inter;
    z-index: 4;
  }

  .description {
    display: flex;
    justify-content: left;
    font-size: 1em;
    position: relative;
    top: -3em;
    color: white;
    font: Inter;
    z-index: 4;
  }

  .scene {
    width: 100%;
    z-index: 4;
  }

  @media (max-width: 450px) {
    .scene {
      display: none;
    }
  }
</style>
