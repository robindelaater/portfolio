<script>
    /**
    * @type {{ title: string; description: string; url: string; tags: [string]; }}
    */
     export let project;
</script>

<div class="p-4 bg-white shadow-md w-full lg:min-w-[28rem] max-w-lg flex flex-col justify-between rounded-sm">
    <div>
        <p class="text-xl font-semibold">{project.title}</p>
        <p class="mb-2 text-neutral-800">{project.description}</p>
        <a class="font-medium hover:underline block mb-4" href="{project.url}" target="_blank">Go to website</a>
    </div>
   
    <ul class="flex gap-2">
        {#each project.tags as tag}
            <li class="pill-tag">{tag}</li>
        {/each}
    </ul>
</div>