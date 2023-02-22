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
        <div class="flex flex-row ml-8">
            {#each [...links] as [title, url]}
                <div>

                </div>
            {/each}
        </div>
    </nav>
    <slot />
</div>