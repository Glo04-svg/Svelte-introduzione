<script>
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
	<!-- Import font pixelato da Google Fonts -->
	<link href="https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap" rel="stylesheet">
</svelte:head>

{@render children()}



<img src=https://media4.giphy.com/media/v1.Y2lkPTZjMDliOTUyNHlhNjQzc3h2dWs2ZTc5OHJ4czJpcDF4bGxnN3k2b3ljY3U5ZHdocCZlcD12MV9zdGlja2Vyc19zZWFyY2gmY3Q9cw/10a8AOSeP6Rqfu/giphy.gif alt="Cute cat gif" />

<footer>
	<p>© Polimi 2026</p>
</footer>

<style>


      :global(p) {
        color: #ff4ebe;
		font-family: 'Press Start 2P', cursive;

    }
	
	footer {
		text-align: center;
		padding: 10px 30px 15px 30px;
		background-color: #f0f0f0;
	}

:global(body) {
        background-color: #1b1818; 
        color: #fff; 
        margin: 0; 
        font-family: 'Press Start 2P', cursive;
    }

	img {
		display: block;
		margin: 20px auto;
		max-width: 100%;
		height: auto;
		border-radius: 10px;
		
	}
	</style>