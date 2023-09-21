<script>
  import FooterApartment from "../components/footer/footerApartment.svelte";
</script>

<footer>
  <div id="design">
    <div id="footerApartment">
      <FooterApartment />
    </div>
    <a id="apply" href="https://apply.vandyhacks.org">Apply Now</a>
  </div>
  <div class="links">
    <div class="block">
      <a href=https://apply.vandyhacks.org/">Judge Portal</a>
      <br /><br />
      <a href="https://www.asurion.com/">Asurion</a>
      <br /><br />
      <a href="https://xy.vandyhacks.org/">Crossyear</a>
    </div>
    <div class="block">
      <a href="https://www.instagram.com/vandyhacks/">Instagram</a>
      <br /><br />
      <a href="https://www.youtube.com/@vandyhacks3426">Youtube</a>
      <br /><br />
      <a href="https://github.com/VandyHacks">Github</a>
      <br /><br />
      <a href="https://discord.gg/GVsHeNR9j6">Discord</a>
      <br /><br />
      <a href="https://x.com/vandyhacks?s=21&t=gRhN7Dcc5Ae-f-c2JKc0ig"
        >X (Twitter)</a
      >
      <br /><br />
      <a href="https://www.facebook.com/vandyhacks/">Facebook</a>
    </div>
    <div class="block">
      <p>Made with &lt3 by the VandyHacks team</p>
    </div>
  </div>
</footer>

<style>
  footer {
    width: 100vw;
    height: 500px;
    background-color: #0e0e1a;
    text-align: left;
    font-size: 20px;
    position: relative;
    bottom: 0px;
  }
  a {
    color: white;
    text-decoration: none;
  }
  .links {
    position: absolute;
    right: 0;
    display: flex;
  }
  .block {
    margin-top: 45px;
    width: 10vw;
    padding: 5vw;
    color: white;
  }
  #footerApartment {
    position: absolute;
    display: inline-block;
    top: 30px;
  }

  #apply {
    background-color: #1d1743;
    top: 180px;
    left: 168px;
    padding: 34px;
    position: relative;
    border-radius: 10px;
  }

  #apply:hover {
    text-shadow: 0 0 20px rgba(255, 56, 131, 1);
  }

  @media (max-width: 865px) {
    #footerApartment {
      display: none;
    }
    #apply {
      display: none;
    }
  }
</style>
