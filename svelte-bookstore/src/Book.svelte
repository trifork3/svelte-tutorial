<script>
	export let bookTitle;
	export let bookPrice;
	export let bookDescription;
</script>

<main>
	<h2> { bookTitle }</h2>
	<p>{ bookPrice }</p>
	<p>{ bookDescription }</p>
</main>

<style>
	div {
		margin: 1rem;
		box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
	}

	h1 {
		font-size: 1.25 rem;
		margin: 0.25rem 0;
	}

	h2 {
		font-size: 1rem;
		margin: 0.25rem 0;
		color: aqua;
	}

	p {
		margin: 0.25rem 0;
	}
</style>