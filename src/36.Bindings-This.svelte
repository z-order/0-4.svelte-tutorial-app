<script>
	import { onMount } from 'svelte';

	let canvas;

	onMount(() => {
		const ctx = canvas.getContext('2d');
		let frame = requestAnimationFrame(loop);

		function loop(t) { // t variable represents the current timestamp passed to the requestAnimationFrame callback (start from 0 in ms unit).
			frame = requestAnimationFrame(loop);

			const imageData = ctx.getImageData(0, 0, canvas.width, canvas.height);

			for (let p = 0; p < imageData.data.length; p += 4) { // 4 bytes : R + G + B + Alpha
				const i = p / 4; // pixel index
				const x = i % canvas.width; // x coordination of the current p position of the pixel
				const y = i / canvas.width >>> 0; // y coordination of the current p position of the pixel

				const r = 64 + (128 * x / canvas.width) + (64 * Math.sin(t / 1000)); // Math.sin(t / 1000): Spanning from -1 to 1 for a cycle of a sign curve during 6 seconds
				const g = 64 + (128 * y / canvas.height) + (64 * Math.cos(t / 1000)); // Math.cos(t / 1000): The 90-degree phase with a difference value of 0.5 against sin() function.
				const b = 128;

				imageData.data[p + 0] = r;
				imageData.data[p + 1] = g;
				imageData.data[p + 2] = b;
				imageData.data[p + 3] = 255;
			}

			ctx.putImageData(imageData, 0, 0);
		}

		return () => {
			cancelAnimationFrame(frame);
		};
	});
</script>

<h1>36. Bindings / This </h1>

<canvas
	bind:this={canvas}
	width={32}
	height={32}
></canvas>

<style>
	canvas {
		width: 100%;
		height: 100%;
		background-color: #666;
		-webkit-mask: url(/svelte-logo-mask.svg) 50% 50% no-repeat;
		mask: url(/svelte-logo-mask.svg) 50% 50% no-repeat;
	}
</style>
