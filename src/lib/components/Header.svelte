<script>
	export let showContact;
</script>

<header class="sticky top-0 z-20 w-full bg-white/60 backdrop-blur-lg">
	<div class="flex items-center py-4 px-4 container mx-auto">

		<nav class="flex justify-between w-full">
			<p class="font-bold text-lg">Robin de Laater</p>
			<ul class="md:flex items-center gap-6 hidden">
				<li>
					<a href="#about">About</a>
				</li>
				<li>
					<a href="#projects">Projects</a>
				</li>
				<li>
					<button class="bg-black text-white px-4 py-2 rounded-md shadow-sm active:shadow-md hover:shadow-lg transition-all duration-150" on:click={() => { showContact = !showContact }}>{ showContact ? 'Close' : 'Contact' }</button>
				</li>
			</ul>
			<button href="javascript:;" class="block md:hidden" on:click={() => { showContact = !showContact }}>
				<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6 {showContact ? 'hidden' : ''}">
					<path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
				</svg>				
				<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6 {!showContact ? 'hidden' : ''}">
					<path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
				</svg>					
			</button>
		</nav>

	</div>
</header>

<div class="fixed top-0 left-0 bg-white/50 backdrop-blur-lg z-10 w-full h-full flex items-center justify-center {!showContact ? '-translate-x-full' : 'translate-x-0'} transition-all duration-150 md:hidden">
	<ul class="flex flex-col items-center gap-6 container mx-auto">
		<li>
			<a href="#about">About</a>
		</li>
		<li>
			<a href="#projects">Projects</a>
		</li>
		<li>
			<button on:click={() => {showContact = !showContact}}>Contact</button>
		</li>
	</ul>
</div>