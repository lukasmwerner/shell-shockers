<script>
	import placeholder from '$lib/images/placeholder.png';
</script>
<style>
	* {
		font-family: 'Merriweather', serif;
	}
	.pale {
		background: #E7DFD4;
	}
	.hero {
		display: grid;
		width: 100%;
		height: 100vh;
		grid-template-columns: 1fr 1fr;
		margin: 0;
		flex-direction: row;
	}
	.hero #img {
		width: 50vw;
		height: auto;
		background-image: url($lib/images/hero_img.jpeg);
	}
	.hero #text {
		display: flex;
		justify-content: center;
		align-items: center;
		flex-direction: column;
		height: 100%;
		font-size: 2rem;
	}

	.product-hero {
		display: grid;
		grid-template-columns: repeat(7 ,1fr);
		grid-template-rows: repeat(5, 1fr);
		padding: 2rem;
		color: #E7DFD4;
	}	
	.product-a {
		background-color: #AA4465;
		grid-column: 1 / 6;
		grid-row: 1 / 4;	
		padding: 1rem;
	}

	.product-b {	
		background-color: #3E7CB1;
		grid-column: 3 / -1;
		grid-row: 3 / -1;
		padding: 1rem;
	}
</style>
<div class="pale hero">
	<div id="img">
	</div>
	<div id="text">
		<h1>Custom Frames</h1>
	</div>
</div>
<div class="pale product-hero">
	<div class="product-a">
		<h1>Modular Frames</h1>
		<div>
			<img src={placeholder} />
			<img src={placeholder} />
			<img src={placeholder} />
		</div>
	</div>

	<div class="product-b">
		<h1>Pre-Made Kits</h1>
		<div>
			<img src={placeholder} />
			<img src={placeholder} />
			<img src={placeholder} />
		</div>
	</div>
</div>
