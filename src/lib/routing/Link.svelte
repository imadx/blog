<script>
  export let href;

  const gotoHref = (event) => {
    event.preventDefault();
    window.history.pushState({ path: window.location.pathname }, "", href);
    window.dispatchEvent(
      new CustomEvent("app-route-change", {
        detail: { path: href },
      }),
    );
  };
</script>

<a {href} on:click={gotoHref}>
  <slot />
</a>

<style>
  a {
    color: #fff;
  }
</style>
