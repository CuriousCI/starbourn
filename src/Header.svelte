<script>
    export let test;
</script>

<header class={test ? 'black' : 'white'}>
    <h1>STARBOURN STUDIOS</h1>
</header>

<style>
    header {
        position: fixed;
        top: 0;
        left: 0;

        z-index: 10;

        display: flex;
        align-items: center;

        width: 100%;
        height: 100px;

        box-sizing: border-box;
        padding: 0 20px;
    }

    .black {
        background-color: unset;
        color: white;
    }

    .white {
        background-color: white;
        color: black;
    }

    h1 {
        color: inherit;
    }
</style>
