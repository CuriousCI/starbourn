<script>
    import Contact from './Contact.svelte';
</script>

<div id="contacts" class="window flex items-end ">
    <div class="content w-full h-full grid place-items-center md:bg-none">
        <div class="flex flex-col self-end content-center">
            <h1>Get in Touch</h1>
            <p class="text-center">Let the magic begin</p>
        </div>
        <Contact />
    </div>
</div>

<style>
    .window {
        background-image: url('../assets/compressed/7.jpg');
        background-position-y: -20vh;
    }

    .content {
        background: rgb(0, 0, 0);
        background: linear-gradient(
            0deg,
            rgba(0, 0, 0, 1) 50%,
            rgba(0, 0, 0, 0) 100%
        );
    }
</style>
