<script>
 console.log('Hello from SvelteKit!');   
 let { initialCount= $bindable() } = $props();
 let count = $state(initialCount);
 let doubled = $derived(count * 2);
</script>

<h3>Clicks Counter</h3>

<button on:click={() => count++}>
    clicks: {count}
</button>

<span>
    doubled: {doubled}
</span>
