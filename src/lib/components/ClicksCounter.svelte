<script>
 console.log('Hello from SvelteKit!');   
 let count = $state(2);
 let doubled = $derived(count * 2);
</script>

<h3>Clicks Counter</h3>

<button on:click={() => count++}>
    clicks: {count}
</button>

<span>
    doubled: {doubled}
</span>
