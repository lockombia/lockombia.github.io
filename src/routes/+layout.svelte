<script lang="ts">
	import "../app.css";
	import Header from "$lib/components/Header.svelte";

	import { onMount } from "svelte";

	let vantaContainer: HTMLDivElement;

	onMount(() => {
		// @ts-ignore
		const effect = window.VANTA.WAVES({
			el: vantaContainer,
			mouseControls: false,
			touchControls: false,
			gyroControls: false,
			minHeight: 200.0,
			minWidth: 200.0,
			scale: 1.0,
			scaleMobile: 1.0,
			color: 0x552800,
			shininess: 24.0,
			waveHeight: 8.5,
			waveSpeed: 0.5,
			zoom: 1.35,
		});

		return () => effect?.destroy?.();
	});
</script>

<div bind:this={vantaContainer} class="vanta-bg"></div>

<Header />
<slot />

<style>
	.vanta-bg {
		position: fixed;
		top: 0;
		left: 0;
		width: 100vw;
		height: 100vh;
		z-index: -1;
	}
</style>
