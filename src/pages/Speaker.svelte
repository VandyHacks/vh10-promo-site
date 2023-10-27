<script>
  import { slide } from "svelte/transition";
  import MediaQuery from "../MediaQuery.svelte";

  import SpeakerCircle from "../components/speaker/speakerCircle.svelte";
  import Scene from "../components/speaker/scene.svelte";

  let speakers = [
    {
      title: "Keynote Speaker",
      name: "Kathryn Rickmeyer",
      description:
        "Kathryn Rickmeyer is Nashville reporter covering technology and business. Rickmeyer relocated to Nashville in 2020 and joined the Nashville Post as staff reporter. The former television news producer quickly made a name for herself breaking stories on historic tech legislation to eight figure fundraisers. Her work has been cited in national and international outlets such as NBC, the Guardian and Tech Crunch.\n" +
        "Last year, Rickmeyer got the entrepreneurial itch. She left Nashville Post and today is communications consultant working with universities, nonprofits and startups to developing messaging and marketing materials.\n" +
        "Of course, the headline hunter couldn't hang up her reporter hat. She started her own online news outlet —Tennbeat.com, where she continues to cover the local tech and entrepreneur scene. Over the last 12 months, she has broken 30+ stories ranging from a the first female tech founder to raise $1.5 million in 8 hours to new AI innovation studios. More than 8,000 Tennesseans subscribe to the independent publication.\n" +
        "Rickmeyer isn't just committed to telling Nashville's tech stories but helping write them. She has co-organized 15+ technology events — including a web3 event series at Vanderbilt University, moderated 10+ panels — including one at Litecoin's 2022 Global Conference, and is a Board Member for the local chapter of Blacks in Technology.\n",
    },
  ];
</script>

<MediaQuery query="(max-width: 768px)" let:matches>
  <div class="container">
    <div class="flex" class:flex-mobile={matches}>
      <div class="speakerAndText" class:speakerAndText-mobile={matches}>
        <div class="speakercircle" class:speakercircle-mobile={matches}>
          <SpeakerCircle />
        </div>
        <div class="text" class:text-mobile={matches}>
          <div class="title" class:title-mobile={matches}>
            {speakers[0].title}
          </div>
          <div class="name" class:name-mobile={matches}>{speakers[0].name}</div>
          <div class="description">
            {speakers[0].description}
          </div>
        </div>
      </div>
    </div>

    <div class="scene" class:scene={!matches}>
      <Scene />
    </div>
  </div>
</MediaQuery>

<style>
  .container {
    display: block;
    position: relative;
    width: 100vw;
    /* background-color: pink; */
    padding-top: 10vh;
  }

  .flex {
    display: flex;
    flex-direction: row;
  }
  .flex-mobile {
    flex-direction: column;
  }

  .speakerAndText {
    display: flex;
    /* justify-content: space-around; removed because it's messing with the right/left arrow positioning */
    width: 90%;
    height: 100vh;
    margin: 0 auto;

    /* background-color: teal; */
  }

  .speakerAndText-mobile {
    height: 100vh;
    flex-direction: column;
    /* background-color: teal; */
  }
  .speakercircle {
    width: 35%;
    margin: 0 auto;
    display: flex;
    justify-content: center;
    /* float: left; */
    /* padding-left: 7vw; */
  }
  .speakercircle-mobile {
    width: 50%;
    /* height: 5vh; */
  }

  .text {
    width: 50%;
    font-size: 1.5em;
    font-weight: 200;
    /* padding-top: 5vw; */
    display: flex;
    flex-direction: column;
    /* height: 100%;
    padding-right: 7vw; */
    align-self: center;
    justify-content: center;
    text-align: justify;
    color: white;
  }
  .text-mobile {
    font-size: 1.25em;
    width: 100%;
  }

  .title {
    text-shadow: 0 0 7px #fff;
    font-size: 2.5em;
    font-weight: 700;
    margin-bottom: 1vh;
  }

  .title-mobile {
    text-align: center;
  }

  .name {
    font-size: 1.4em;
    font-weight: 700;
    margin-bottom: 1vh;
  }

  .name-mobile {
    font-size: 1.4em;
    font-weight: 700;
    margin-bottom: 1vh;
    text-align: center;
  }
  .description {
    height: 50%;
    overflow-y: scroll;
  }

  .scene {
    height: 50%;
    width: 100%;
    z-index: 4;
  }
</style>
