<script>
    import Contact from './Contact.svelte';
</script>

<div id="contacts" class="window">
    <div class="content">
        <div class="title">
            <h1>Get in Touch</h1>
            <p>Let the magic begin</p>
        </div>
        <Contact />
    </div>
</div>

<style>
    .window {
        background-image: url('../assets/compressed/7.jpg');
        background-position-y: -20vh;

        display: flex;
        align-items: flex-end;
    }

    .content {
        width: 100%;
        height: 60vh;

        display: grid;
        place-items: center;

        background: rgb(0, 0, 0);
        background: linear-gradient(
            0deg,
            rgba(0, 0, 0, 1) 50%,
            rgba(0, 0, 0, 0) 100%
        );
    }

    .title {
        display: flex;
        flex-direction: column;
        align-self: flex-end;
        justify-content: center;
    }

    .title p {
        text-align: center;
    }
</style>
