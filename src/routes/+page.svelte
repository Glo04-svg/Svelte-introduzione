<script>
  import { website } from "$lib/state.svelte.js";
  import ClicksCounter from "$lib/components/ClicksCounter.svelte";
  import CanvasSquare from "$lib/components/CanvasSquare.svelte";
  import TodoList from "$lib/components/TodoList.svelte";
  import TitleEditor from "$lib/components/TitleEditor.svelte";

  let count = $state(5);
  console.log("Ciao MERDE!");
</script>

<div class="flex-content">
  <div class="centered-content">
    <h1>{website.title}</h1>
    <p>
      Visit <a href="https://svelte.dev/docs/kit">svelte.dev/docs/kit</a> to read
      the documentation
    </p>

    <TitleEditor />

    <ClicksCounter bind:initialCount={count} />

    {#if count > 10 && count < 20}
      <p>count from parent is {count}</p>
    {:else if count > 30}
      <p>that's a lot of clicks!</p>
    {:else}
      <p>count from parent is not in range</p>
    {/if}

    <CanvasSquare />

    <TodoList />
  </div>
  <img
    src="https://media4.giphy.com/media/v1.Y2lkPTZjMDliOTUyNHlhNjQzc3h2dWs2ZTc5OHJ4czJpcDF4bGxnN3k2b3ljY3U5ZHdocCZlcD12MV9zdGlja2Vyc19zZWFyY2gmY3Q9cw/10a8AOSeP6Rqfu/giphy.gif"
    alt="Cute cat gif"
  />
</div>

<style>
  h1 {
    color: rgb(255, 230, 251);
    font-family: "Press Start 2P", cursive;
  }

  .flex-content {
    display: flex;
    gap: 2em;
    align-items: center;
    justify-content: center;
    height: 90vh;
  }

  .centered-content {
    margin: 0 auto;

    max-width: fit-content;
  }
  img {
    display: block;
    margin: 20px auto;
    max-width: 100%;
    height: auto;
    border-radius: 10px;
  }
</style>
