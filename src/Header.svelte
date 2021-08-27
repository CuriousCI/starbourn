<script>
    export let scrollY, menus;

    $: scrolling = scrollY >= 50;
    $: menu = menus[Math.floor(scrollY / window.innerHeight)];
</script>

<header
    class:invert={scrolling}
    class="hidden md:visible w-screen h-24 md:grid md:grid-cols-3 z-10 fixed items-center px-10"
>
    <h1 class="col-span-1">STARBOURN STUDIOS</h1>
    <nav
        class="col-span-2 flex items-center justify-evenly box-border"
        role="navigation"
    >
        {#each menus as section}
            <a
                class:border-b-2={menu == section}
                class="font-semibold"
                href="#{section}"
                on:click={() => (menu = section)}
            >
                {section}
            </a>
        {/each}
    </nav>
</header>

<style>
    .invert {
        background-color: white;
        color: black;
    }
</style>
