<script>
    import ProductPage from "$lib/components/ProductPage.svelte";
	import acrylic from "$lib/images/acrylic.png";
	import corner from "$lib/images/corner.png";
	import cover from "$lib/images/cover.png";
	import corner_cover from "$lib/images/cover_corner.png";
	import everything from "$lib/images/everything.jpg";
	import hanging from "$lib/images/hanging.png";
	import side_piece from "$lib/images/side_piece.png";

	let title = "Modular Picture Frames";
	let description = `<p><b>Modular Frame</b></p>

<p>Instead of one large frame, the modular frame is comprised of several pieces. This means you can resize your frame, and you won’t have to buy a whole new one! It really is the last frame you’ll ever have to buy. </p>

<p><b>Hanging System</b></p>

<p>The adjustable hanging system removes many of the frustrations associated with hanging a picture frame. It uses a sawtooth hanger that can be moved up and down, meaning you won’t have to reposition any more nails. It can also be reused between frames!</p>

<p><b>Snap-On Frame Borders</b></p>

<p>Add personalization to your picture frame with snap-on frame borders! You can get a set of colored or patterned pieces that magnetize right onto your modular frame, making it easy to customize its appearance.</p>

<p><b>Accessible Frame Backing</b></p>

<p>Our frame backing uses a retaining clip instead of metal tabs, making it easier to remove and change out your pictures. </p>`;

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
<ProductPage images={[everything, acrylic, corner, cover, corner_cover, hanging, side_piece]} {products} {title} {description} />
