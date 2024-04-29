<style>
	:root {
		background: #E7DFD4;
		font-family: 'Merriweather', serif;
	}
	.product {
		display: flex;
		flex-direction: row;
		background: #E7DFD4;
		min-height: 100vh;
		height: 100%;
	}
	.split {
		max-width: 50vw;
		padding: 2rem;
	}
	.text {
		background-color: #6A8D73;
	}
	.previews {
		padding-top: 10px;
	}
	.previews img {
		height: 10vh;
		width: auto;
	}
	.images .large {
		display: flex;
		justify-items: center;
		align-items: center;
		width: 100%;
	}
	.images .large img {
		width: 50vw;
		height: auto;
	}
	@media (max-width: 1200px) {
		.images {
			padding-bottom: 0;
		}
		.product {
			display: contents;
			background-color: red;
			height: auto;
			min-height: auto;
		}
		.split {max-width: none;}

		.text {
			background: #E7DFD4;
		}

		.images .large img {
			width: 100%;
		}
	}
</style>

<script>
import AddToCart from '$lib/components/AddToCart.svelte';

/** @type Array<string> */
export let images = [];
let activeImg = 0;

export let title = "";
export let description = "";

/** @type Array<any> */
export let products = [];

</script>

<div class="product">
	<div class="split images">
		<div class="large">
			<img src={images[activeImg]} />
		</div>
		<div class="previews">
			{#each images as image, i}
				<img src={image} on:click={() => activeImg = i}/>
			{/each}
		</div>
	</div>
	<div class="split text">
		<h1>{title}</h1>
		{@html description}

		{#each products as product}
			<AddToCart name={product.name} cost={product.cost} dynamic={product.dynamic} costFunction={product.costFunction} />
		{/each}
	</div>
</div>
