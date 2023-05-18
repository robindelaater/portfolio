<script>
	import Header from '$lib/components/Header.svelte';
  	import FeaturedBlock from "$lib/components/FeaturedBlock.svelte";
  	import IntroSection from "$lib/components/IntroSection.svelte";
	import PurpleBlob from "$lib/components/PurpleBlob.svelte";
	import Footer from '$lib/components/Footer.svelte';

	let showContact = false;
	$: showContact;

	const data = [
		{
			title: 'Comfort Club Clothing',
			description: 'Development of their new Shopify store including the integration of a wishlist and stock notifier.',
			tags: ['Liquid', 'VueJS', 'Shopify', 'Sass', 'JS'],
			url: 'https://comfortclubclothing.com'
		},
		{
			title: 'Kicksshop.nl',
			description: 'New shop built on Lightspeed for kicksshop.nl',
			tags: ['Twig', 'VueJS', 'JS', 'CSS'],
			url: 'https://kicksshop-demo.webshopapp.com'
		},
		{
			title: 'SOV Media',
			description: 'Web design and development for SOV Media. Including API integration with a CMS for easy customisability.',
			tags: ['SvelteKit', 'TailwindCSS', 'Netlify', 'JS', 'CSS'],
			url: 'https://sov-media.com'
		},
		{
			title: 'MultiSafepayJS',
			description: 'NPM module for easier integration with the MultiSafepay payments API.',
			tags: ['TypeScript', 'NPM'],
			url: 'https://github.com/robindelaater/multisafepay-js'
		},
		{
			title: 'Pim Cauwels',
			description: 'Web design and development for photographer Pim Cauwels. API integration with a CMS for easy customisation.',
			tags: ['SvelteKit', 'TailwindCSS', 'Netlify'],
			url: 'https://pimcauwels.nl/'
		}
	]
</script>

<Header bind:showContact />

<main class="container mx-auto">
	<IntroSection bind:showContact />

	<section id="projects" class="flex flex-col py-8">
		<h4 class="text-xl sm:text-2xl md:text-3xl font-semibold mb-6">Featured projects</h4>

		<div class="flex gap-4 flex-wrap sm:flex-col lg:flex-row">
			{#each data as project}
			<FeaturedBlock {project} />
			{/each}
		</div>
	</section>

	<section id="about" class="flex flex-col py-8">
		<h4 class="text-3xl font-semibold mb-6">About me</h4>
		<p class="max-w-2xl text-lg">
			<span class="font-medium">Hello! I'm Robin de Laater, a 22-year-old full-stack web developer with expertise in e-commerce, payments, and shipping.</span> With a passion for crafting exceptional online experiences, I combine technical skills with a keen eye for design. Beyond coding, I find joy in playing guitar, exploring the automotive world, and pushing my limits at the gym. <br><br> <span class="pointer-events-auto cursor-pointer hover:italic" on:click={() => { showContact = !showContact }}>Let's collaborate to bring your digital vision to life!</span>
		</p>
	</section>
</main>

<Footer />

<PurpleBlob />

<div class="bg-white w-full h-full fixed top-0 left-0 z-10 transition-all duration-200 flex flex-col items-center justify-center p-4 {showContact ? 'translate-x-0' : 'translate-x-full'}">
	<h4 class="text-2xl font-semibold mb-2 text-center">What can I do for you?</h4>
	<form action="" class="contact-form flex flex-col">
		<label for="name">
			Name
			<input type="text" name="name">
		</label>
		<label for="email">
			Email
			<input type="email" name="email">
		</label>
		<label for="tel">
			Phonenumber
			<input type="phone" name="phone">
		</label>
		<label for="message">
			What can I do for you?
			<textarea name="message"></textarea>
		</label>
		<button class="button-lg flex items-center gap-2" on:click={() => { showContact = !showContact }}>
            <svg class="w-5 h-5" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" >
                <path stroke-linecap="round" stroke-linejoin="round" d="M7.5 8.25h9m-9 3H12m-9.75 1.51c0 1.6 1.123 2.994 2.707 3.227 1.129.166 2.27.293 3.423.379.35.026.67.21.865.501L12 21l2.755-4.133a1.14 1.14 0 01.865-.501 48.172 48.172 0 003.423-.379c1.584-.233 2.707-1.626 2.707-3.228V6.741c0-1.602-1.123-2.995-2.707-3.228A48.394 48.394 0 0012 3c-2.392 0-4.744.175-7.043.513C3.373 3.746 2.25 5.14 2.25 6.741v6.018z" />
            </svg>
            Let's connect 
        </button>
	</form>
</div>