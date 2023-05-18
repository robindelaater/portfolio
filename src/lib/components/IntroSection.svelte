<script>
    export let showContact
</script>

<section class="intro flex flex-col py-8">
    <h1 class="text-2xl md:text-4xl lg:text-6xl mb-8">
        Enthusiastic web developer with a creative mindset, constantly exploring new technologies and
        dedicated to delivering impactful online solutions.
    </h1>
    <div class="flex gap-4 items-center">
        <button class="button-lg flex items-center gap-2" on:click={() => { showContact = !showContact }}>
            <svg class="w-5 h-5" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" >
                <path stroke-linecap="round" stroke-linejoin="round" d="M7.5 8.25h9m-9 3H12m-9.75 1.51c0 1.6 1.123 2.994 2.707 3.227 1.129.166 2.27.293 3.423.379.35.026.67.21.865.501L12 21l2.755-4.133a1.14 1.14 0 01.865-.501 48.172 48.172 0 003.423-.379c1.584-.233 2.707-1.626 2.707-3.228V6.741c0-1.602-1.123-2.995-2.707-3.228A48.394 48.394 0 0012 3c-2.392 0-4.744.175-7.043.513C3.373 3.746 2.25 5.14 2.25 6.741v6.018z" />
            </svg>
            Let's connect 
        </button>
        <a class="text-button-lg" href="#about">About me</a>
    </div>
</section>