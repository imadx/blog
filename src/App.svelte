<main>
  <div class="badge">This blog is a work in progress</div>
  <hgroup>
    <h1>Ishan Madhusanka</h1>
    <h2>Software Developer, Solutions Architect, UI/UX Ehtnusiast</h2>
  </hgroup>

  <!-- <div class="message">
    <input type="text" placeholder="Send me a message" />
    <button> Send </button>
  </div> -->

  <div>
    <button>Projects</button>
    <button>Blog</button>
  </div>
</main>
<svg viewBox="0 0 720 700" fill="none" xmlns="http://www.w3.org/2000/svg">
  <path
    opacity="0.45"
    d="M720 0C600 109 436.238 -24.253 334 137C231.762 298.253 551.085 418.183 571.044 323.986C591.003 229.79 153.458 213.439 142.795 393.75C132.131 574.061 397.728 476.234 373.28 593.411C348.832 710.588 98.7929 578.361 1 700"
    stroke="#D9D9D9"
    stroke-width="1"
    stroke-dasharray="12 12"
  />
</svg>

<footer>
  Ishan Madhusanka. Copyright &copy; {new Date().getFullYear()}
</footer>

<style lang="scss">
  :root {
    font-family: "Inter", sans-serif;
    height: 100%;
  }

  :global(html) {
    background-color: #2b2a33;
    color: #fff;
  }

  :global(html, body) {
    margin: 0;
    height: 100%;
  }

  :global(*) {
    box-sizing: border-box;
  }

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
      font-size: 1.2rem;
      font-weight: normal;
    }
  }

  footer {
    height: 3rem;
    font-size: 1rem;
    opacity: 0.7;
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

  svg {
    position: absolute;
    top: 0;
    left: 0;
    height: 100%;
    width: 100%;
    pointer-events: none;
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
