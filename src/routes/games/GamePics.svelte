<script>
	// @ts-nocheck

	import sewsew1 from '$lib/assets/games/sewsew1.png';
	import sewsew2 from '$lib/assets/games/sewsew2.png';
	import sewsew3 from '$lib/assets/games/sewsew3.png';
	import sewsew4 from '$lib/assets/games/sewsew4.png';

	import maymorning1 from '$lib/assets/games/maymorning1.png';
	import maymorning2 from '$lib/assets/games/maymorning2.png';
	import maymorning3 from '$lib/assets/games/maymorning3.png';
	import maymorning4 from '$lib/assets/games/maymorning4.png';

	import eartrainer1 from '$lib/assets/games/eartrainer1.png';
	import eartrainer2 from '$lib/assets/games/eartrainer2.png';

	import colorfulworld1 from '$lib/assets/games/colorfulworld1.png';
	import colorfulworld2 from '$lib/assets/games/colorfulworld2.png';
	import colorfulworld3 from '$lib/assets/games/colorfulworld3.png';
	import colorfulworld4 from '$lib/assets/games/colorfulworld4.png';

	import otde1 from '$lib/assets/games/otde1.png';
	import otde2 from '$lib/assets/games/otde2.png';
	import otde3 from '$lib/assets/games/otde3.png';
	import otde4 from '$lib/assets/games/otde4.png';
	import { onMount } from 'svelte';

	export let gameId;

	let show = false;
	onMount(() => (show = true));

	const imagesById = {
		sewsew: {
			pics: [
				{ src: sewsew1, alt: 'animated woman working at a desk in a paper home' },
				{ src: sewsew2, alt: 'close-up of paper desk with a laptop, vase, and book' },
				{ src: sewsew4, alt: 'close-up of table with sewing machine and cutting board' }
			]
		},
		maymorning: {
			width: 250,
			pics: [
				{ src: maymorning1, alt: 'pixel art bedroom with deep blues' },
				{
					src: maymorning3,
					alt: 'pixel art backyard with text "a big, beautiful bleeding heart bush"'
				},
				{ src: maymorning4, alt: 'pixel art backyard with text "you water a tomato plant!"' }
			]
		},
		eartrainer: {
			bordered: true,
			width: 375,
			pics: [
				{ src: eartrainer1, alt: 'digital metronome and a guessing notepad' },
				{ src: eartrainer2, alt: 'metronome again, with settings display to the left' }
			]
		},
		colorfulworld: {
			pics: [
				{
					src: colorfulworld1,
					alt: 'greyscale characters in greyscale world talk to each other about mission to restore color'
				},
				{
					src: colorfulworld2,
					alt: 'greyscale character is turned yellow when hit by flying color ball, in industrial environment'
				},
				{
					src: colorfulworld3,
					alt: 'malicious (but silly) looking, tall figure with cane emerges from platform'
				}
			]
		},
		otde: {
			pics: [
				{
					src: otde1,
					alt: 'cartoon scuba divers on a dock are shocked as one diver is grabbed by giant crab'
				},
				{
					src: otde3,
					alt: 'underwater submarine is bombarded by various hermit crabs, showing signs of damage'
				},
				{
					src: otde4,
					alt: 'diving characters fight giant underwater crab, holding captured diver'
				}
			]
		}
	};
</script>

<div class="wrapper">
	{#each imagesById[gameId].pics as imageObj}
		<img
			src={imageObj.src}
			alt={imageObj.alt}
			width={imagesById[gameId].width || 300}
			class:bordered={imagesById[gameId].bordered}
			class:show
			loading="lazy"
		/>
	{/each}
</div>

<style>
	.wrapper {
		display: flex;
		flex-wrap: wrap;
		gap: 15px;
		margin-bottom: 20px;
	}
	img {
		height: 200px;
		/* width: 300px; */
		object-fit: cover;
		border-radius: 8px;
		opacity: 0;
		transition: opacity 1s ease;
	}
	img.show {
		opacity: 1;
	}
	.bordered {
		border: 1px solid rgba(0, 0, 0, 0.1);
	}
</style>
