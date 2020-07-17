<script>
	export let name;
	let count = 0;
	$: doubled = count * 2;
	function handleClick(){
		count += 1;
	}
</script>

<main>
	<h1>Hello {name}!</h1>
	<button on:click={handleClick}>
	You clicked {count} {count===1?'time':'times'}
	</button>
	<p>{count} doubled is {doubled}</p>
	<p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>
	<h2>Let off some steam, Bennett!</h2>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		/* color: #ff3e00; */
		color: orange;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	h2 {
		color: green;
		font-family: courier, monospace;
		/* font-family: 'Comic Sans MS', cursive; */
		/* font-size: 2em; */
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>