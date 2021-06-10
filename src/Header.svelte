<script>
    export let scrollY, menus;

    $: scrolling = scrollY >= 50;
    $: menu = menus[Math.floor(scrollY / window.innerHeight)];
</script>

<header class:invert={scrolling}>
    <h1>STARBOURN STUDIOS</h1>
    <nav role="navigation">
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

    @media screen and (max-width: 992px) {
        header {
            display: none;
        }
    }

    nav {
        display: flex;
        align-items: center;
        justify-content: space-evenly;

        box-sizing: border-box;
    }

    .invert {
        background-color: white;
        color: black;
    }

    .selected {
        border-bottom: 2px solid;
        border-color: inherit;
    }

    a {
        height: 100%;

        color: inherit;
        text-decoration: unset;

        font-weight: bolder;
        font-size: 1.2vw;
    }
</style>
