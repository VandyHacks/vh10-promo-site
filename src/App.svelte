<script>
  import Home from "./pages/Home.svelte";
  import About from "./pages/About.svelte";
  import Speaker from "./pages/Speaker.svelte";
  import FAQ from "./pages/FAQ.svelte";
</script>

<div class="all">
  <Home />
  <About />
  <Speaker />
  <FAQ />
</div>

<style lang="postcss" global>
  .all {
    display: grid;
    grid-template-columns: repeat(1, auto);
    grid-template-rows: repeat(3, 1fr);
  }
</style>
