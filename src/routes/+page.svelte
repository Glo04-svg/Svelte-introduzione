<script>
import ClicksCounter from '$lib/components/ClicksCounter.svelte';
import ProgressiveSum from '$lib/components/ProgressiveSum.svelte';
console.log('Ciao MERDE!');
let count = $state(5);
</script> 

<h1>Welcome to SvelteKit, GLO!</h1>
<p>Visit <a href="https://svelte.dev/docs/kit">svelte.dev/docs/kit</a> to read the documentation</p>

<ClicksCounter bind:initialCount={count} />

  <p>
    count from parent is {count} 

  </p>   


<style> 

    h1 {
        color: rgb(255, 230, 251);
        font-family: 'Press Start 2P', cursive;
    }
  
</style>