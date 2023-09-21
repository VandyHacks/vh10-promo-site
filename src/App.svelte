<script>
  import Home from "./pages/Home.svelte";
  import About from "./pages/About.svelte";
  import Schedule from "./pages/Schedule.svelte";
  import Speaker from "./pages/Speaker.svelte";
  import FAQ from "./pages/FAQ.svelte";
  import Sponsors from "./pages/Sponsors.svelte";
  import Footer from "./pages/Footer.svelte";
</script>

<div class="all">
  <Home />
  <About />
  <Schedule />
  <Speaker />
  <FAQ />
  <Sponsors />
  <Footer />
</div>

<style lang="postcss" global>
  .all {
    display: grid;
    grid-template-columns: repeat(1, auto);
    grid-template-rows: repeat(6, 1fr);
  }
</style>
