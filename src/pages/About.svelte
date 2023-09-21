<script>
  import AboutMountain_1 from "../components/about/about_mountain_1.svelte";
</script>

<div style="position: relative; display: flex; justify-content: space-around;">
  <div class="text-container">
    <div class="about_title">About VH X</div>
    <div class="about_desc">
      Lorem Ipsum is simply dummy text of the printing and typesetting industry.
      Lorem Ipsum has been the industry's standard dummy text ever since the
      1500s, when an unknown printer took a galley of type and scrambled it to
      make a type specimen book.<br /><br />It has survived not only five
      centuries, but also the leap into electronic typesetting, remaining
      essentially unchanged. It was popularised in the 1960s with the release of
      <br /><br />Letraset sheets containing Lorem Ipsum passages, and more
      recently with desktop publishing software like Aldus PageMaker including
      versions of Lorem Ipsum.
    </div>
  </div>

  <div class="right-container">
    <div class="main-img-container">
      <img src="/img/groupphoto.png" alt="group photo" />
      <div class="mountain1_svg">
        <AboutMountain_1 />
      </div>
    </div>
    <div class="miniature-container">
      <img src="/img/miniature1.png" class="miniature-img" alt="miniature 1" />
      <img src="/img/miniature2.png" class="miniature-img" alt="miniature 2" />
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
  .about_desc {
    width: 40vw;
    color: white;
    font: Inter;
    font-size: 1.5em;
    font-weight: 200;
    word-wrap: break-word;
  }

  /* Container styles */
  .main-img-container {
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
