<script>
	let sitename = "junior job";
	const handleClick = () => {
		sitename = 'an updated site name';
	}

	let apiData;

	const fetchData = async () => {
	try {
		const r = await fetch('http://localhost:8080/api/login');
		if (r.ok) {
		apiData = await r.json();
		} else {
		console.error('Error getting api data', r.statusText);
		}
	} catch (e) {
		console.error('Error gettinng api data:', e.message);
	}
	};
</script>

<main>
	<h1>Welcome to {sitename}</h1>
	<p>Welcome to the very first version of my Svelte frontend site</p>
	<button on:click={handleClick}>Update site name</button>

	<button on:click={fetchData}>Fetch Data</button>
  
	{#if apiData}
	  <pre>{JSON.stringify(apiData, null, 2)}</pre>
	{/if}
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>