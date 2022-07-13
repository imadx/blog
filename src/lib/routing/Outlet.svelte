<script lang="ts">
  import { onMount } from "svelte";

  let modules = import.meta.glob("../../pages/**");

  let defaultModule = import.meta.glob("../../pages/index.svelte").default;
  let element = defaultModule;

  onMount(() => {
    window.addEventListener("popstate", function (event) {
      updatePath();
    });

    window.addEventListener("app-route-change", () => {
      updatePath();
    });
  });

  const updatePath = () => {
    const getSanitized = (path: string): string => {
      let _path = path.split("/pages")[1];
      _path = _path.replace("index.svelte", "");
      _path = _path.replace(".svelte", "");

      return _path;
    };

    let matchDeviation = 1;
    let matchedElement = null;

    let timeout = null;

    const updateElement = () => {
      clearTimeout(timeout);
      timeout = setTimeout(() => {
        element = matchedElement;
      }, 0);
    };

    for (const path in modules) {
      modules[path]().then((mod) => {
        const sanitizedPath = getSanitized(path);
        const pathname = window.location.pathname;

        if (pathname.includes(pathname)) {
          const distance = Math.abs(sanitizedPath.length - pathname.length);
          if (distance <= matchDeviation) {
            matchDeviation = distance;
            matchedElement = mod.default;
            updateElement();
          }
        }
      });
    }
  };

  updatePath();
</script>

<svelte:component this={element} />
