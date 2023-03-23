<script>
	import Header from '../lib/components/Header.svelte';
	import AboutSection from '../lib/components/AboutSection.svelte';
</script>

<section class="sticky top-0 bg-gradient-to-tr from-indigo-500 to-purple-400">
	<Header />

	<div class="flex flex-col relative md:flex-row sm:justify-center w-full container mx-auto px-4">
		<p
			class="font-bold text-xl md:text-4xl lg:text-6xl leading-normal text-white self-center mb-12 md:mb-auto"
		>
			Hi! My name is Robin de Laater.<br /> A <i>creative developer</i> who loves starting new projects.
		</p>
		<img
			class="self-end w-24 md:w-1/2 -z-10 absolute bottom-0 md:relative"
			src="/memoji.png"
			alt="🦍"
		/>
	</div>
</section>

<AboutSection />

<section class="sticky z-10 bg-white">
	<div class="container mx-auto px-4 py-12">
		<p class="text-2xl font-semibold mb-2">Projects</p>

		<div class="projects grid md:grid-flow-col md:grid-cols-3 gap-4">
			<a class="project-card" href="https://sov-media.com" target="_blank">
				<img class="project-card__image" src="/sov-media.png" alt="" />
				<div
					class="absolute z-10 top-0 left-0 flex flex-col justify-center items-center bg-neutral-900/50 w-full h-full"
				>
					<p class="text-2xl text-white">SOVMedia</p>
					<p class="text-white">Design & development</p>
				</div>
			</a>

			<a
				class="project-card"
				href="https://www.npmjs.com/package/@robindelaater/multisafepay-js"
				target="_blank"
			>
				<img class="project-card__image" src="/multisafepayjs.png" alt="" />
				<div
					class="absolute z-10 top-0 left-0 flex flex-col justify-center items-center bg-neutral-900/50 w-full h-full"
				>
					<p class="text-2xl text-white">MultiSafepayJS</p>
					<p class="text-white">Development</p>
				</div>
			</a>

			<a class="project-card" href="https://pimcauwels.nl" target="_blank">
				<img class="project-card__image" src="/pimcauwels.png" alt="" />
				<div
					class="absolute z-10 top-0 left-0 flex flex-col justify-center items-center bg-neutral-900/50 w-full h-full"
				>
					<p class="text-2xl text-white">Pim Cauwels</p>
					<p class="text-white">Development</p>
				</div>
			</a>
		</div>
	</div>
</section>

<section class="sticky top-0 z-20 bg-neutral-800">
	<div
		class="container mx-auto flex flex-col items-center justify-center text-center py-12 px-4 gap-4"
	>
		<p class="text-white font-bold text-2xl md:text-4xl">Don't be shy, get in touch.</p>
		<p class="text-white mb-4">
			Wanna grab a cup of joe and chat about all the awesome stuff we could create together?
		</p>
		<a
			href="mailto:robin@delaater.nl"
			class="bg-gradient-to-tr from-indigo-400 to-purple-500 text-white rounded-md py-2 px-4 font-semibold text-lg hover:shadow-lg hover:shadow-purple-500/10 hover:bg-gradient-to-tr hover:from-indigo-500 hover:to-purple-400 transition-all duration-150"
			>Contact me</a
		>
	</div>
</section>

<footer class="bg-neutral-900">
	<div class="container mx-auto flex items-center py-4 md:py-8 px-4">
		<p class="text-neutral-600">&copy; Robin de Laater 2023</p>
	</div>
</footer>
