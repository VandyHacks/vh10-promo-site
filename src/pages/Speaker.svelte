<script>
  import { slide } from "svelte/transition";
  import MediaQuery from "../MediaQuery.svelte";

  import SpeakerCircle from "../components/speaker/speakerCircle.svelte";
  import Scene from "../components/speaker/scene.svelte";

  let speakers = [
    {
      title: "Speaker Series",
      name: "Co-President Alex Oh",
      description:
        "Alex Oh is a junior at Vanderbilt University and is a really cool dude. Like a really cool dude. He is also one of the Co-Presidents of VandyHacks X. This is another sentence talking about how awesome he is.",
    },
    {
      title: "Speaker Series",
      name: "Co-President Maya",
      description:
        "Maya is a junior at Vanderbilt University and is really cool. Like a really cool. She is also one of the Co-Presidents of VandyHacks X. This is another sentence talking about how awesome she is.",
    },
    // Add more speakers as needed
  ];

  let currentIndex = 0;

  function goPrev() {
    if (currentIndex > 0) currentIndex--;
  }

  function goNext() {
    if (currentIndex < speakers.length - 1) currentIndex++;
  }
</script>

<MediaQuery query="(max-width: 768px)" let:matches>
  <div class="container" class:container-mobile={matches}>
    <div class="speakerAndText">
      <!--left button-->
      {#if currentIndex > 0}
        <button
          class="switchSpeakerRight"
          style="color: white;"
          on:click={goPrev}>&lt;</button
        >
      {:else}
        <button class="switchSpeakerLeft" style="color: grey;">&lt;</button>
      {/if}

      <div class="speakercircle">
        <SpeakerCircle />
      </div>

      <div
        class="text"
        transition:slide={{
          delay: 250,
          duration: 300,
          axis: "x",
        }}
      >
        <!-- logic for changing names and description -->
        <div class="title">{speakers[currentIndex].title}</div>
        <div class="name">{speakers[currentIndex].name}</div>
        <div>
          {speakers[currentIndex].description}
        </div>
      </div>

      <!--right button-->
      {#if currentIndex != speakers.length - 1}
        <button
          class="switchSpeakerRight"
          style="color: white;"
          on:click={goNext}>&gt;</button
        >
      {:else}
        <button class="switchSpeakerRight" style="color: grey;">&gt;</button>
      {/if}
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
    /* todo: figure out a better way to do this, 
    this creates a weird gap between sections in mobile */
  }
  .container-mobile {
    height: 60vh;
  }
  .speakerAndText {
    display: flex;
    /* justify-content: space-around; removed because it's messing with the right/left arrow positioning */
    width: 100%;
    height: 50vh;
  }
  .switchSpeakerLeft {
    background-color: transparent;
    border: none;
    font-size: 2em;
    padding-left: 1vw;
  }
  .switchSpeakerRight {
    background-color: transparent;
    border: none;
    font-size: 2em;
    padding-right: 1vw;
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

  @media (max-width: 865px) {
    .scene {
      display: none;
    }
  }
</style>
