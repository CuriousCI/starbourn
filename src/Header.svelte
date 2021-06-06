<script>
    export let scrolling,
        menus,
        menu = 'Home';
</script>

<header class={scrolling ? 'invert' : ''}>
    <h1>STARBOURN STUDIOS</h1>
    <nav>
        {#each menus as section}
            <a
                class="pointer {menu == section ? 'selected' : ''}"
                href="#{section}"
            >
                {section}
            </a>
            <!-- <span
                class="pointer {menu == section ? 'selected' : ''}"
                on:click={() => (menu = section)}
            >
                {section}
            </span> -->
        {/each}
    </nav>
</header>

<style>
    header {
        position: fixed;
        z-index: 1;

        display: grid;
        grid-template-columns: 1fr 2fr;
        align-items: center;

        width: 100%;
        height: 100px;

        box-sizing: border-box;
        padding: 0 20px;
    }

    nav {
        display: flex;
        align-items: center;
        justify-content: space-evenly;

        box-sizing: border-box;
        padding: 0 100px;
    }

    .invert {
        background-color: white;
        color: black;
        border-color: black;
    }

    .selected {
        border-bottom: 2px solid inherit;
    }

    a {
        color: inherit;
    }
</style>
