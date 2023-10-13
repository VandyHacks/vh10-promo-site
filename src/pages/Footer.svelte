<script>
  import MediaQuery from "../MediaQuery.svelte";
  import FooterApartment from "../components/footer/footerApartment.svelte";
</script>

<MediaQuery query="(max-width: 768px)" let:matches>
  <div class="container" class:container-mobile={matches}>
    <div class="design">
      <div class="footerApartment">
        <FooterApartment />
        <div class="apply">
          <a href="https://apply.vandyhacks.org" class="applyLink">Apply Now</a>
        </div>
        
      </div>
    </div>
    <div class="links">
      <div class="block">
        <a href="https://apply.vandyhacks.org/">Judge Portal</a>
        <br /><br />
        <a href="https://www.asurion.com/">Asurion</a>
        <br /><br />
        <a href="https://xy.vandyhacks.org/">Crossyear</a>
      </div>
      <div class="break"></div>
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
  </div>
</MediaQuery>

<style>
  a {
    color: white;
    text-decoration: none;
  }
  .links {
    position: absolute;
    display: flex;
    right: 10vw;
    padding: 10px;
  
  }
  .container {
    width: 100vw;
    height: 100vh; 
    background-color: #0e0e1a;
    text-align: left;
    font-size: 1.5em;
    position: relative;
    bottom: 0px;
    margin: 0;
  }
  .block {
    width: 10vw;
    padding: 5vw;
    color: white;

  }
  .footerApartment {
    position: absolute;
    width: 20vw;
    height:auto;
    top: 60px;
  }

  .apply {
    background-color: #1d1743;
    border-radius: 10px;
    width: 10vw;
    height: 7vw;
    top: 26%;
    left: 60%;
    position: absolute;
    display: flex;
    flex-direction: column;
    align-items: center; /* Vertically center content */
    justify-content: center;
  }

    .applyLink{
      width: auto;
      height: auto;
      margin: 0; /* Remove margin */
      font-size: 2vw;
      white-space: nowrap;
    }

  /* .apply:hover {
    text-shadow: 0 0 20px rgba(255, 56, 131, 1);
  } */

  @media (max-width: 865px) {
    .links{
      flex-direction: column;
      position: static;
    
    }
    .break{
      height: 2px;
      background-color: white;
    }
    .block{
      width: 70vw;
      text-align: left;
      padding-left: 0;
    }
    .container{
      height: auto;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      white-space: nowrap;
      font-size: 4vw;
    }
    
    .design{
      z-index: 1;
      order: 2;
      position: relative;
      bottom: 30px;
    }

    .footerApartment{
      top: 0;
      width: 50vw;
      height: auto;
      position: relative;
    }

    .apply{
      top: 25%;
      left: 30vw;
      width: 30vw;
      height:20vw;
      padding: 0%;
    }

    .applyLink{
      width: auto;
      height: auto;
      margin: 0; 
      font-size: 5vw;
      white-space: nowrap;
    }
  }

</style>
