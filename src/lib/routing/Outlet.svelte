<script>
  let modules = import.meta.glob("../../pages/**");
  let element = null;

  for (const path in modules) {
    modules[path]().then((mod) => {
      const pathname = window.location.pathname;
      if (path.includes(pathname)) {
        element = mod.default;
      }
    });
  }
</script>

<svelte:component this={element} />
<slot />
