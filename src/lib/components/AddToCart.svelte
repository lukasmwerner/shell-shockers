<script>
export let dynamic = false;
export let cost = "";
export let costFunction = (a, b) => a;
export let name = "";

let width;
let height;

function compute(w, h) {
	if (width == undefined || height == undefined) {
		return '';
	}
	w = new Number(w);
	h = new Number(h);
	let f = costFunction(w, h);
	console.log(f, w, h)
	return  `$${f}`;
}

$: displayCost = compute(width, height)

function addToCart() {

}

</script>


<div class="buy">
	{#if dynamic}
		<input placeholder="Width" bind:value={width}/>
		<input placeholder="Height" bind:value={height}/>
	{/if}
	<span class="btn" on:click={addToCart}>Add {name} {dynamic ? displayCost : cost}</span>
</div>


<style>
	.buy {
		padding: 0.2em;
		display: flex;
		flex-direction: row;
		background-color: #E7DFD4;
		border-radius: 20px;
		margin: 0.2em;
		padding-left: 1em;
	}
	.buy input {
		background-color: #E7DFD4;
		border: none;
	}
	.buy .btn {
		display: flex;
		flex-direction: row;
		padding: 1rem;
		align-items: center;
		justify-content: center;
	}
@media (max-width: 1200px) {
.buy  {
	background-color: #6A8D73;
	color: #E7DFD4;
}
.buy input {
	background-color: #6A8D73;
	color: #E7DFD4;
}
.buy input::placeholder {
	color: #a5a099;
}
}
</style>
