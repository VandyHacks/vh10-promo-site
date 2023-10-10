<script>
  import { Router, Route } from "svelte-routing";

  import Main from "./pages/Main.svelte";
  import Asurion from "./pages/Asurion.svelte";
</script>

<Router>
  <Route path="/" component={Main} />
  <Route path="/asurion" component={Asurion} />
</Router>

<style lang="postcss" global>
</style>
