<script>
	import { onMount } from 'svelte';
	let results = [];
	onMount(() => {
		getGiftCards();
	});

	const getGiftCards = async () => {
		fetch('https://jsonplaceholder.typicode.com/posts')
			.then((response) => response.json())
			.then((json) => {
				console.log(json);
				results = json.map((el) => el.title);
			});
	};
</script>

<svelte:head />
<main class="response">
	<h1>Posts</h1>
	{#each results as result}
		<p>{result}</p>
	{/each}
</main>
