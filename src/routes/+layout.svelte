<script>
  import favicon from "$lib/assets/favicon.svg";
  let { children } = $props();
</script>

<svelte:head>
  <link rel="icon" href={favicon} />
  <!-- Import font pixelato da Google Fonts -->
  <link
    href="https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap"
    rel="stylesheet"
  />
</svelte:head>

{@render children()}

<footer>
  <p>© Polimi 2026</p>
</footer>

<style>
  :global(p) {
    color: #ff4ebe;
    font-family: "Press Start 2P", cursive;
  }

  footer {
    text-align: center;
    padding: 10px 30px 15px 30px;
    width: 100%;
    background-color: #f0f0f0;
    margin-top: auto;
    height: 10vh;
  }

  :global(body) {
    background-color: #1b1818;
    color: #fff;
    margin: auto;
    font-family: "Press Start 2P", cursive;
  }

  img {
    display: block;
    margin: 20px auto;
    max-width: 100%;
    height: auto;
    border-radius: 10px;
  }
</style>
