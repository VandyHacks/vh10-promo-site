<script>
  import VHlogo from "../components/home/VHlogo.svelte";
  import FirstCloud from "../components/home/firstCloud.svelte";
  import SecondCloud from "../components/home/secondCloud.svelte";
  import ThirdCloud from "../components/home/thirdCloud.svelte";
  import FourthCloud from "../components/home/fourthCloud.svelte";
  import FifthCloud from "../components/home/fifthCloud.svelte";
  import MLHBadge from "../components/home/MLHBadge.svelte";
</script>

<MLHBadge />

<div class="container">
  <div>
    <div class="logo">
      <VHlogo />
    </div>
    <div class="title">VANDYHACKS X</div>
    <div class="date">October 28 - 29 | Nashville, TN</div>
    <div class="outer">
      <div class="middle">
        <div class="inner">
          <a href="https://apply.vandyhacks.org" target="_blank">
            <div class="apply">Apply Now</div>
          </a>
        </div>
      </div>
    </div>
  </div>

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

<style>
  .container {
    display: block;
    position: relative;
    width: 100vw;
    height: 100vh;
  }
  .logo {
    display: flex;
    justify-content: center;
    z-index: 4;
  }

  .title {
    display: flex;
    justify-content: center;
    text-shadow: 0 0 7px #fff;
    color: white;
    font-size: 3em;
    font-weight: 700;
    position: relative;
    top: -2em;
    font: Inter;
    z-index: 4;
  }

  .date {
    display: flex;
    justify-content: center;
    font-size: 1.4em;
    position: relative;
    top: -4em;
    color: #e0e1f5;
    font: Inter;
    z-index: 4;
  }

  .outer {
    display: flex;
    justify-content: center;
    margin-top: 60px;
    position: relative;
    top: -6em;
  }

  .middle {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 160px;
    height: 30px;
    border: 2px solid #ffffff;
    box-shadow: 0 0 7px #fff;
    z-index: 2;
  }

  .inner {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 140px;
    height: 20px;
    border: 2px solid #ffffff;
    box-shadow: 0 0 7px #fff;
    z-index: 2;
  }

  .apply {
    color: white;
    font: Inter;
    text-shadow: 0 0 4px #fff;
    z-index: 2;
  }

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
