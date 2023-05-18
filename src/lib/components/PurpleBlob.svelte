<script>
    import { onMount } from 'svelte';
	import anime from 'animejs'

	onMount(() => {
		anime({
			targets: '#purple-blob',
			scale: 1.3,
			duration: 30000,
			loop: true,
			rotate: '360deg', 
			direction: 'alternate',
			easing: 'easeOutQuad'
		})
	})
</script>

<div class="colors-bg fixed -z-20 w-[100vw] h-[100vh] top-0">
	<svg id="purple-blob" width="950" height="950" viewBox="0 0 950 950" fill="none" xmlns="http://www.w3.org/2000/svg">
	<g filter="url(#filter0_f_1_15)">
	<path d="M688.75 619C657.25 715 593.5 750 497.5 724C401.5 698 315.25 650 238.75 580C162.25 510 162.25 439.75 238.75 369.25C315.25 298.75 396.75 259 483.25 250C569.75 241 633.5 276.25 674.5 355.75C715.5 435.25 720.25 523 688.75 619Z" fill="url(#paint0_radial_1_15)"/>
	</g>
	<defs>
	<filter id="filter0_f_1_15" x="0" y="0" width="950" height="950" filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB">
	<feFlood flood-opacity="0" result="BackgroundImageFix"/>
	<feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape"/>
	<feGaussianBlur stdDeviation="50" result="effect1_foregroundBlur_1_15"/>
	</filter>
	<radialGradient id="paint0_radial_1_15" cx="0" cy="0" r="1" gradientUnits="userSpaceOnUse" gradientTransform="translate(26576.6 24432.8) scale(26395.2 24184.2)">
	<stop stop-color="#444CF7"/>
	<stop offset="1" stop-color="#C244F7" stop-opacity="0.2"/>
	</radialGradient>
	</defs>
	</svg>
</div>
