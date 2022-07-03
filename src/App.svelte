<script>
  import HomeArtwork from "./lib/artwork/HomeArtwork.svelte";
  import Button from "./lib/shared/Button.svelte";
  import Footer from "./lib/layout/Footer.svelte";
  import Badge from "./lib/shared/Badge.svelte";
</script>

<main>
  <Badge>This blog is a work in progress</Badge>
  <hgroup>
    <h1>Ishan Madhusanka</h1>
    <h2 title="I'm a human">
      U29mdHdhcmUgRGV2ZWxvcGVyLCBTb2x1dGlvbnMgQXJjaGl0ZWN0LCBVSS9VWCBFbnRodXNpYXN0
    </h2>
  </hgroup>

  <!-- <div class="message">
    <input type="text" placeholder="Send me a message" />
    <button> Send </button>
  </div> -->

  <div>
    <Button>Projects</Button>
    <Button>Blog</Button>
  </div>
</main>

<HomeArtwork />
<Footer />

<style lang="scss">
  hgroup {
    h1,
    h2 {
      margin: 0;
    }
  }

  main,
  footer {
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

  h1 {
    font-size: 3rem;
    font-weight: bold;
  }

  p {
  }

  .message {
    background: #42414d;
    padding: 0.5rem 1rem;
    box-shadow: 0 0.875rem 1.25rem rgba(0, 0, 0, 0.25);
    border-radius: 0.313rem;
    display: flex;
    max-width: 30rem;

    input {
      background-color: transparent;
      border: none;
      color: #fff;
      font-size: 1rem;
      padding: 1rem;
      margin: -1rem;
      margin-right: 0;
      flex: 1;
    }
  }

  button {
    background: #7257e3;
    border-radius: 0.25rem;
    color: #fff;
    border: none;
    padding: 0.5rem 1rem;
    font-size: 1rem;
    cursor: not-allowed;
  }

  .badge {
    background: #ffb62c;
    width: fit-content;
    padding: 0.5rem;
    color: #2b2a33;
    font-weight: bold;
    border-radius: 5px;
  }
</style>
