<script>
  import { slide } from "svelte/transition";
  import MediaQuery from "../MediaQuery.svelte";

  import SpeakerCircle from "../components/speaker/speakerCircle.svelte";
  import Scene from "../components/speaker/scene.svelte";

  let speakers = [
    {
      title: "Keynote Speaker",
      name: "Lacie Thorne",
      description:
        "Lacie Thorne is a dynamic professional who has seamlessly transitioned from the world of fashion to the tech industry. With a foundation in Fashion Design from Parsons School of Design, Lacie pursued her commitment to her career pivot by recently graduating with her MBA with a focus on Sustainability from Yale School of Management.\n" +
        "Her career has taken her across the globe, with significant roles in both New York City and Hong Kong. Currently, as a Product Manager in tech in New York City, Lacie leads Agile projects and champions user-centered design, enhancing technology solutions for users with intuitive, seamless experiences.\n" +
        "In addition to her tech role, Lacie is an educator, serving as a Faculty Instructor at Belmont University's O'More School of Design, where she empowers aspiring designers and marketers. Her journey is punctuated by numerous accolades, including the prestigious Yale School of Management Entrepreneurship Fellowship, the Yale Climate Innovation Grant, and the Visa®️ Digital Creators Program, highlighting her dedication to innovation and sustainability in both fashion and technology.\n",
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
    height: 75vh;
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
    height: 70%;
    overflow-y: scroll;
  }

  .scene {
    height: 50%;
    width: 100%;
    z-index: 4;
  }
</style>
