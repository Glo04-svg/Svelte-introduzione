<script>
import ClicksCounter from '$lib/components/ClicksCounter.svelte';
import CanvasSquare from '$lib/components/CanvasSquare.svelte';
  import TodoList from '$lib/components/TodoList.svelte';
let count = $state(5);
console.log('Ciao MERDE!');

</script> 

<h1>Welcome to SvelteKit, GLO!</h1>
<p>Visit <a href="https://svelte.dev/docs/kit">svelte.dev/docs/kit</a> to read the documentation</p>

<ClicksCounter bind:initialCount={count} />


{#if count > 10 && count < 20}
     <p> count from parent is {count} </p>
{:else if count > 30}
     <p> that's a lot of clicks! </p>
{:else}
     <p> count from parent is not in range </p>
{/if}
 
<CanvasSquare />

<TodoList />

<style> 

    h1 {
        color: rgb(255, 230, 251);
        font-family: 'Press Start 2P', cursive;
    }
  
</style>