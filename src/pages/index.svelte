<script lang="ts">
  import HomeArtwork from "src/lib/artwork/HomeArtwork.svelte";
  import Link from "src/lib/routing/Link.svelte";

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
    <Link href="/projects">
      <Button>Projects</Button>
    </Link>
    <Link href="/blog">
      <Button>Blob</Button>
    </Link>
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
    display: flex;
    flex-direction: column;
    justify-content: center;
    gap: 2rem;
    min-height: calc(100vh - 19rem);

    h2 {
      font-size: 0.8rem;
      font-weight: normal;
    }
  }
</style>
