<script>
  import HomeArtwork from "src/lib/artwork/HomeArtwork.svelte";

  import Badge from "src/lib/shared/Badge.svelte";
  import Button from "src/lib/shared/Button.svelte";
</script>

<main>
  <Badge>This blog is a work in progress</Badge>
  <hgroup>
    <h1>Ishan Madhusanka</h1>
    <h2 title="I'm a human">
      U29mdHdhcmUgRGV2ZWxvcGVyLCBTb2x1dGlvbnMgQXJjaGl0ZWN0LCBVSS9VWCBFbnRodXNpYXN0
    </h2>
  </hgroup>

  <div>
    <Button>Projects</Button>
    <Button>Blog</Button>
  </div>
</main>
<HomeArtwork />

<style lang="scss">
  hgroup {
    h1,
    h2 {
      margin: 0;
    }
  }

  main {
    padding: 1em;
  }

  main {
    min-height: calc(100vh - 3rem);
    display: flex;
    flex-direction: column;
    gap: 2rem;
    justify-content: center;

    h2 {
      font-size: 0.8rem;
      font-weight: normal;
    }
  }
</style>
