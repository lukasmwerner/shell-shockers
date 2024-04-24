<script>
    import ProductPage from "$lib/components/ProductPage.svelte";
	import one from "$lib/images/modular-frames/a.jpg";
	import two from "$lib/images/modular-frames/b.jpg";
	let title = "Modular Picture Frames";
	let description = `Ea sunt id adipisicing. Ad et elit ullamco deserunt anim laborum aute magna ex ex aliqua et ut officia. Dolor velit dolor quis occaecat deserunt. Officia enim cupidatat proident et aute incididunt commodo aute velit cupidatat ipsum officia exercitation ad. Excepteur esse excepteur ut culpa proident elit eu eiusmod laboris nisi cillum eiusmod veniam deserunt consectetur.
Proident ullamco aliqua Lorem velit occaecat occaecat culpa nisi dolor velit. Pariatur tempor sit labore cillum cillum amet amet. Eu enim adipisicing nisi id ea non eiusmod tempor dolore officia. Officia duis exercitation pariatur consequat officia commodo anim Lorem voluptate. Id fugiat irure incididunt ex nisi magna in esse velit aliqua id eiusmod sint.`;

	let products = [
		{name: "Acrylic", dynamic: true, cost: "$0.00/ct", costFunction: (w, h) => 0.03*(w*h) },
		{name: "Frame Backing", dynamic: true, cost: "$0.00/ct", costFunction: (w, h) => 0.09*(w*h) + 0.23 },
		{name: "Hanging System", cost: "$5.50/ct"},
		{name: "Frame Side", cost: " $0.54/ct"},
		{name: "Frame Corner", cost: "$2.56/ct"},
		{name: "Snap on Frame Side Borders", cost: "$0.14/ct"},
		{name: "Snap on Frame Corner Borders", cost: "$0.66/ct"},
	]
</script>
<ProductPage images={[one, two]} {products} {title} {description} />
