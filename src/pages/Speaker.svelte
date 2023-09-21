<script>
  import MediaQuery from "../MediaQuery.svelte";

  import SpeakerCircle from "../components/speaker/speakerCircle.svelte";
  import Scene from "../components/speaker/scene.svelte";
</script>

<MediaQuery query="(max-width: 768px)" let:matches>
  <div class="container" class:container-mobile={matches}>
    <div class="speakerAndText">
      <div class="speakercircle">
        <SpeakerCircle />
      </div>

      <div class="text">
        <div class="title">Speaker Series</div>
        <div class="name">Co-President Alex Oh</div>
        <div>
          Alex Oh is a junior at Vanderbilt University and is a really cool
          dude. Like a really cool dude. He is also one of the Co-Presidents of
          VandyHacks X. This is another sentence talking about how awesome he
          is.
        </div>
        <!-- implement logic for changing names and description -->
      </div>
    </div>

    <div class="scene">
      <Scene />
    </div>
  </div>
</MediaQuery>

<style>
  .container {
    display: block;
    position: relative;
    width: 100vw;
    height: 150vh;
  }
  .container-mobile {
    height: 60vh;
  }
  .speakerAndText {
    display: flex;
    justify-content: space-around;
    width: 100%;
    height: 50vh;
  }
  .speakercircle {
    width: 30%;
    float: left;
    padding-left: 7vw;
  }
  .text {
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    height: 100%;
    width: 40%;
    font-size: 1.5em;
    font-weight: 200;
    padding-right: 7vw;
    color: white;
  }
  .title {
    text-shadow: 0 0 7px #fff;
    font-size: 2.5em;
    font-weight: 700;
  }

  .name {
    font-size: 1.4em;
    font-weight: 700;
  }

  .scene {
    position: absolute;
    width: 100%;
    z-index: 4;
  }

  @media (max-width: 768px) {
    .scene {
      display: none;
    }
  }
</style>
