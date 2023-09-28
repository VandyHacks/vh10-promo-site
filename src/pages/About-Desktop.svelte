<script>
  import AboutLeftMountains from "../components/aboutLeftMountains.svelte";
  import AboutRightMountains from "../components/aboutRightMountains.svelte";
  import AboutMountain_1 from "../components/about/about_mountain_1.svelte";
</script>

<div style="position: relative; display: flex; justify-content: space-around;">
  <div class="text-container">
    <div class="about_title">About VH X</div>
    <div class="about_desc">
      VandyHacks, Vanderbilt's premier student-run hackathon, proudly stands as
      the largest collegiate hackathon in the South. Celebrating our 10th
      edition, VandyHacks X invites global participants to immerse in 24
      electrifying hours of innovation, from October 28-29.
      <br /><br />
      Set against a vibrant neon theme, this fully in-person event beckons hackers
      to craft groundbreaking projects, attend illuminating workshops, explore career
      opportunities, and vie for coveted prizes.
      <br /><br />
      Join us, and let's light up the future together!
    </div>
  </div>

  <div class="right-container">
    <div class="main-img-container mountain-img-container">
      <img src="/img/groupphoto.png" alt="group photo" />
      <div class="mountain1_svg">
        <AboutMountain_1 />
      </div>
    </div>
    <div class="miniature-container">
      <div class="mountain-img-container">
        <img
          src="/img/miniature1.png"
          class="miniature-img"
          alt="miniature 1"
        />
        <div class="leftmountain_svg">
          <AboutLeftMountains />
        </div>
      </div>
      <div class="mountain-img-container">
        <img
          src="/img/miniature2.png"
          class="miniature-img"
          alt="miniature 2"
        />
        <div class="rightmountain_svg">
          <AboutRightMountains />
        </div>
      </div>
    </div>
  </div>
</div>

<style>
  .text-container {
    flex: 1;
    max-width: calc(100% / 3);
    padding: 20px;
  }

  .about_title {
    color: #fff;
    text-shadow: 0 0 7px #fff;
    font-family: Inter;
    font-size: 2.5em;
    font-style: normal;
    font-weight: 700;
    line-height: normal;
  }
  .about_desc {
    width: 40vw;
    color: white;
    font-size: 1.5em;
    font-weight: 200;
    word-wrap: break-word;
  }

  /* Container styles */
  .mountain-img-container {
    position: relative;
    height: min-content;
  }

  .main-img-container img {
    width: 550px;
    object-fit: cover;
    z-index: 0;
  }

  .mountain1_svg {
    position: absolute;
    z-index: 1;
    bottom: -25px;
    width: 200px;
    left: -85px;
  }

  .leftmountain_svg {
    position: absolute;
    z-index: 1;
    bottom: -40px;
    width: 145px;
    left: -60px;
  }
  .rightmountain_svg {
    position: absolute;
    z-index: 1;
    bottom: -17px;
    width: 148px;
    right: -52px;
  }

  .right-container {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .miniature-container {
    margin-top: 50px;
    display: flex;
    justify-content: space-around;
    width: 100%;
  }

  .miniature-img {
    width: 175px;
    object-fit: cover;
    border-radius: 50%;
  }
</style>
