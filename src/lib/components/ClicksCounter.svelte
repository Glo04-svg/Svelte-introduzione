<script>
 console.log('Hello from SvelteKit!');   
 let { initialCount:count= $bindable() } = $props();

 let doubled = $derived(count * 2);
</script>

<h3>Clicks Counter</h3>

<button onclick={() => count++}>
    clicks: {count}
</button>

<span>
    doubled: {doubled}
</span>
