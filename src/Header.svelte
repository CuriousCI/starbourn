<script>
    export let scrolling, menus;
    let menu = 'Home';
</script>

<header class:invert={scrolling}>
    <h1>STARBOURN STUDIOS</h1>
    <nav>
        {#each menus as section}
            <a
                class:selected={menu == section}
                href="#{section}"
                on:click={() => (menu = section)}
            >
                {section}
            </a>
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
    }

    .selected {
        color: red;
    }
</style>
