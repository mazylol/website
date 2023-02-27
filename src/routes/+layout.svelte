<script>
    import "../app.css"

    const links = new Map([
        ['Home', '/'],
        ['Projects', '/projects'],
        ['About', '/about']
    ])
</script>

<div class="bg-neutral-700 min-h-screen">
    <nav class="w-full bg-neutral-800">
        <div class="flex flex-row h-16 ml-2 justify-center">
            {#each [...links] as [title, url]}
                <div class="mx-2 mt-3 text-gray-200 text-3xl font-bold">
                    <a href={url} class="px-2 py-1 hover:bg-gray-200 hover:text-neutral-800 rounded-xl transition-all duration-100">{title}</a>
                </div>
            {/each}
        </div>
    </nav>
    <slot />
</div>