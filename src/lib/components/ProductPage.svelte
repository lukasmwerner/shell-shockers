<style>
	:root {
		background: #E7DFD4;
		font-family: 'Merriweather', serif;
	}
	.product {
		display: flex;
		flex-direction: row;
		background: #E7DFD4;
		height: 100vh;
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
	.buy {
		padding: 4rem;
	}
	.buy .btn {
		background-color: #E7DFD4;
		border-radius: 20px;
		display: flex;
		flex-direction: row;
		padding: 1rem;
		align-items: center;
		justify-content: center;
	}
	@media (max-width: 1200px) {
		.images {
			padding-bottom: 0;
		}
		.product {
			display: contents;
			background-color: red;
			height: auto;
		}
		.split {max-width: none;}

		.text {
			background: #E7DFD4;
		}

		.buy .btn {
			background-color: #6A8D73;
			color: #E7DFD4;
		}
		.images .large img {
			width: 100%;
		}
	}
</style>

<script>
/** @type Array<string> */
export let images = [];
let activeImg = 0;

export let title = "";
export let description = "";
export let cost = "";

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
		<p>{description}</p>

		<div class="buy">
			<span class="btn">Add {cost}</span>
		</div>
	</div>
</div>
