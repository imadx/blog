<script>
  import Link from "../routing/Link.svelte";
  let isHomeButtonVisible = location.pathname !== "/";

  window.addEventListener("app-route-change", () => {
    isHomeButtonVisible = location.pathname !== "/";
  });
</script>

<header>
  {#if isHomeButtonVisible}
    <Link href="/">Home</Link>
  {/if}
</header>

<style lang="scss">
  header {
    padding: var(--padding-default);
  }
</style>
