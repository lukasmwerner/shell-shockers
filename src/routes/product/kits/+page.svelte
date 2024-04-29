<script>
    import ProductPage from "$lib/components/ProductPage.svelte";
	import assembly from "$lib/assembly.gif";
	import group from "$lib/images/kits/prototype_group.jpg";
	import everything from "$lib/images/everything.jpg";
	let title = "Modular Picture Frame Kits";
	let description = `<p>Introducing the ultimate picture framing solution - the Modular Framing Kit! This innovative system gives you unmatched flexibility and customization for displaying your cherished memories.</p>
<p>At the heart of the kit is the Modular Frame itself. Instead of being locked into a single, rigid frame size, this unique design is comprised of several interconnecting pieces that allow you to easily resize the frame. Whether you need it larger or smaller, you can configure the ideal dimensions in minutes without buying an entirely new frame. It's the last frame you'll ever need!</p>
<p>Hanging your framed pictures has never been easier thanks to the Adjustable Hanging System included. No more struggling with re-positioning nails or damaging your walls. The sawtooth hanger can slide up and down to achieve the perfect height, and it can be transferred between different Modular Frames for versatile use.</p>
<p>Customize the look of your frame with the decorative Snap-On Frame Borders. This set of colored and patterned border pieces use built-in magnets to securely attach right onto the Modular Frame, letting you switch up the style as often as you'd like.</p>
<p>Finally, the Accessible Frame Backing eliminates frustration when changing out photos. Instead of fiddly metal tabs, it features a simple retaining clip that allows you to easily remove the backing and swap in new pictures whenever desired.</p>
<p>With its unparalleled modularity, adjustable hanging system, stylish customizations, and frustration-free design, the Modular Framing Kit offers everything you need to display your memories in a way that perfectly suits your style and space. Framing made easy!</p>`;

	let products = [
		{name: "Frame", dynamic: true, costFunction: (w, h)=> {
				let cost = 0;
				cost += 0.03*(w*h); // Acrylic
				cost += 0.09*(w*h) + 0.23; // Backing
				cost += 5.50; // Hanging System
				cost += 0.54*(Math.ceil(w-3)+Math.ceil(h-3));// straight frame
				cost += 10.24; // corner frame
				cost += 0.14*(Math.ceil(w-3)+Math.ceil(h-3));// straight cover 
				cost += 2.64; // corner cover
				return cost;
		}},
	]
</script>
<ProductPage images={[group, assembly, everything]} {products} {title} {description} />
