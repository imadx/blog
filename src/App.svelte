<script>
  import Footer from "./lib/layout/Footer.svelte";
  import Header from "./lib/layout/Header.svelte";
  import Outlet from "./lib/routing/Outlet.svelte";
</script>

<Header />
<main>
  <Outlet />
</main>
<Footer />

<style lang="scss">
  main {
    padding: var(--padding-default);
    min-height: calc(100vh - 3rem);
  }
</style>
