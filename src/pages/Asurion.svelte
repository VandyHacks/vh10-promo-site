<script>
  import MediaQuery from "../MediaQuery.svelte";
  import { link } from "svelte-routing";

  import Sponsor1 from "../components/sponsors/sponsor1.svelte";

  import FirstCloud from "../components/home/firstCloud.svelte";
  import SecondCloud from "../components/home/secondCloud.svelte";
  import ThirdCloud from "../components/home/thirdCloud.svelte";
  import FourthCloud from "../components/home/fourthCloud.svelte";
  import FifthCloud from "../components/home/fifthCloud.svelte";
</script>

<MediaQuery query="(max-width: 768px)" let:matches>
  <div class="container">
    <!-- back button -->
    <a href="/" use:link>
      <div class="button">Back</div>
    </a>

    <!-- Asurion page -->
    <div class="asurion-container">
      <!-- Asurion logo -->
      <div class="asurion-logo">
        <Sponsor1 />
      </div>

      <!-- About asurion -->
      <div class="title-text">
        <div class="title">About Asurion</div>
        <div class="text">
          Asurion helps more than 350 million people around the world unlock
          their technology's untapped potential. We create innovative technology
          solutions that help keep consumers connected, from comprehensive
          protection to smart tech help that redefines expertise. Partnering
          with leading wireless carriers, retailers and pay-tv providers,
          Asurion's 22,000 employees and counting, deliver a seamless,
          award-winning customer experience, anticipating their needs and
          providing tailored services reachable within one touch.
        </div>
      </div>

      <!-- Build your career -->
      <div class="title-text">
        <div class="title">Build your career at Asurion</div>
        <div class="text">
          <div>For 2024 summer internships, we are looking for:</div>
          <!-- list the internships -->
          <div class="list">
            <div>&gt; Software Engineer</div>
            <div>&gt; DevOps Engineer</div>
            <div>&gt; UX Design</div>
            <div>&gt; Data Science (Master's/PhD level)</div>
            <div>&gt; Accounting/Audit</div>
            <div>&gt; Financial Planning & Analysis</div>
            <div>&gt; Secrutiy & Risk</div>
          </div>
        </div>
      </div>

      <!-- Apply now -->
      <a href="https://careers.asurion.com/us/en" target="_blank">
        <div class="button apply-now">Apply Now!</div>
      </a>

      <!-- Duck stickers -->
      <img
        src="/img/duck1.png"
        alt="duck"
        class="duck duck-1"
        class:duck-mobile={matches}
      />
      <img
        src="/img/duck2.png"
        alt="duck"
        class="duck duck-2"
        class:duck-mobile={matches}
      />
      <img
        src="/img/duck3.png"
        alt="duck"
        class="duck duck-3"
        class:duck-mobile={matches}
      />
      <img
        src="/img/duck4.png"
        alt="duck"
        class="duck duck-4"
        class:duck-mobile={matches}
      />
    </div>

    <!-- Background Cloud -->
    <div class="firstCloud">
      <FirstCloud />
    </div>

    <div class="secondCloud">
      <SecondCloud />
    </div>

    <div class="thirdCloud">
      <ThirdCloud />
    </div>

    <div class="fourthCloud">
      <FourthCloud />
    </div>

    <div class="fifthCloud">
      <FifthCloud />
    </div>
  </div>
</MediaQuery>

<style>
  .container {
    display: block;
    position: relative;
    width: 100vw;
    height: 100vh;
    color: white;
  }

  .asurion-container {
    width: 80vw;
    left: 10vw;
    right: 10vw;
    background-color: rgba(0, 0, 0, 0.9);
    border-radius: 20px;
    position: absolute;
    z-index: 3;
  }
  .asurion-logo {
    margin: 5%;
  }
  .title-text {
    padding: 40px;
    padding-bottom: 0;
  }
  .title {
    font-size: 1.5em;
    font-weight: 700;
  }
  .text {
    font-size: 1em;
    font-weight: 300;
    margin-top: 20px;
  }
  .list {
    margin-top: 20px;
  }
  /* add bullet point before */
  .list > div {
    margin-left: 20px;
    margin-top: 10px;
  }

  /* Buttons */
  .button {
    background-color: rgba(255, 255, 255, 0.25);
    width: 111px;
    height: 40px;
    text-align: center;
    line-height: 40px;
    border-radius: 5px;
    margin: 20px;
    color: white;
  }
  .apply-now {
    width: 200px;
    margin-left: 40px;
    margin-bottom: 40px;
  }
  .button:hover {
    cursor: pointer;
  }

  /* Ducks */
  .duck {
    position: absolute;
    width: 150px;
  }
  .duck-1 {
    top: 10px;
    left: calc(75px + 60%);
  }
  .duck-2 {
    right: -50px;
    bottom: 10%;
  }
  .duck-3 {
    bottom: 5%;
    left: 70%;
  }
  .duck-4 {
    bottom: 30%;
    left: 60%;
  }
  .duck-mobile {
    width: 50px;
    right: 0;
  }

  /* Background cloud */
  .firstCloud {
    position: absolute;
    left: -100px;
    top: 50px;
    z-index: 1;
  }

  .secondCloud {
    position: absolute;
    left: 20px;
    top: 680px;
    z-index: 1;
  }

  .thirdCloud {
    position: absolute;
    left: 400px;
    top: 780px;
    z-index: 1;
  }

  .fourthCloud {
    position: absolute;
    right: 50px;
    top: 450px;
    z-index: 1;
  }

  .fifthCloud {
    position: absolute;
    right: -100px;
    top: 50px;
    z-index: 1;
  }
</style>
