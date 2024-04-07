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
		text-align: center;
		height: 100%;
		font-size: 2rem;
	}
	.product-hero {
		display: grid;
		grid-template-columns: repeat(7 ,1fr);
		grid-template-rows: repeat(5, 1fr);
		padding: 2rem;
		color: #E7DFD4;
		height: 100%;
	}	
	.product-hero a {
		color: #E7DFD4;
		text-decoration: none;
	}
	.product-hero .imgs {
		height: 100%;
	}
	.product-hero img {
		height: auto;/*40%;*/
		width: auto;
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
	.mobile-only {
		display: none;
	}

	@media (max-width: 1020px) {
		.hero #img {
			display: none;
		}
		.hero #text {
			grid-column: 1 / -1;	
			/*background-image: url($lib/images/hero_img.jpeg);*/
		}
		.product-hero {
			display:flex;
			flex-direction: column;
		}
		.product-a {
			margin: 0.5rem;
		}
		.product-b {
			margin: 0.5rem;
		}
		.mobile-hidden {
			display: none;
		}
		.mobile-only {
			display: block;
		}
	}
</style>
<div class="pale hero">
	<div id="img">
	</div>
	<div id="text">
		<h1>Custom Frames</h1>
		<p class="mobile-only">Bringing Some Color to Your Walls</p>
	</div>
</div>
<div class="pale product-hero">
	<div class="product-a">
		<a href="/product/modular-frames"><h1>Modular Frames →</h1></a>
		<div class="imgs">
			<img src={placeholder} />
			<img src={placeholder} />
			<img src={placeholder} class="mobile-hidden"/>
		</div>
	</div>

	<div class="product-b">
		<a href="/product/kits"><h1>Pre-Made Kits →</h1></a>
		<div class="imgs">
			<img src={placeholder} />
			<img src={placeholder} />
			<img src={placeholder} class="mobile-hidden"/>
		</div>
	</div>
</div>
