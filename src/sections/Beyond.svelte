<div id="beyond" class="window">
    <div class="content">
        <div>
            <h1>Imagine Beyond</h1>
            <p>
                Creative - Ideation & Planning<br />
                Content Production & Creation<br />
                Distribution & Marketing
            </p>
        </div>
    </div>
</div>

<style>
    .window {
        background-image: url('../assets/compressed/5.jpg');
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
            rgba(0, 0, 0, 1) 50%,
            rgba(0, 0, 0, 0) 100%
        );
    }

    @media (min-width: 992px) {
        .window {
            align-items: center;
            justify-content: flex-end;
            background-position-y: 0;
        }

        .content {
            width: 70vw;
            height: 100%;

            justify-content: flex-end;

            background: rgb(0, 0, 0);
            background: linear-gradient(
                270deg,
                rgba(0, 0, 0, 1) 50%,
                rgba(0, 0, 0, 0) 100%
            );

            box-sizing: border-box;
            padding-right: 5vw;
        }
    }
</style>
