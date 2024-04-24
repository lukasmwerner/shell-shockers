<style>
:root {
	margin: 0;
	padding: 0;
	background: black;
}
video {
	height: 100vh;
	width: 100vw;
}
</style>
<script>
import vid from '$lib/assembly.mp4';
</script>
<video autoplay loop controls>
	<source src={vid} type="video/mp4" />
</video>
