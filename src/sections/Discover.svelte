<div id="discover" class="window">
    <div class="content">
        <div>
            <h1>Discover Us</h1>
            <p>
                Content Creation<br />
                Video Production<br />
                Post Production<br />
                Commercial<br />
                Corporate<br />
                Print & Digital
            </p>
        </div>
    </div>
</div>

<style>
    .window {
        background-image: url('../assets/compressed/4.jpg');
        background-position-y: -20vh;

        display: flex;
        align-items: flex-end;
    }

    .content {
        width: 100%;
        height: 40vh;

        display: grid;
        place-items: center;

        background: rgb(0, 0, 0);
        background: linear-gradient(
            0deg,
            rgba(0, 0, 0, 1) 80%,
            rgba(0, 0, 0, 0) 100%
        );
    }

    @media (min-width: 992px) {
        .window {
            align-items: center;
            background-position-y: 0;
        }

        .content {
            width: 70vw;
            height: 100%;

            justify-content: flex-start;

            background: rgb(0, 0, 0);
            background: linear-gradient(
                90deg,
                rgba(0, 0, 0, 1) 50%,
                rgba(0, 0, 0, 0) 100%
            );

            box-sizing: border-box;
            padding-left: 5vw;
        }
    }
</style>
