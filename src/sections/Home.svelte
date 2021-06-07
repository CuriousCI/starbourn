<div id="home" class="window">
    <h1>
        We bring ideas to life!<br />
        Stories to entertain the<br />
        audience around the world
    </h1>
    <p>
        "Storytelling is the most powerful way to put<br />
        ideas into the world today." --Robert McKee
    </p>
</div>

<style>
    .window {
        background-image: url('../assets/compressed/1.jpg');

        display: grid;
        grid-template-rows: 8.5fr 1fr;
        place-items: center;
    }

    h1 {
        font-size: 27px;
    }

    p {
        font-size: 15px;
        align-self: flex-start;
    }

    @media (min-width: 992px) {
        h1 {
            justify-self: flex-start;

            font-size: 70px;
            margin-left: 5vw;
        }

        p {
            font-size: 26px;
        }

        p br {
            display: none;
        }
    }

    @media (min-width: 1200px) {
        h1 {
            font-size: 80px;
        }
    }
</style>
