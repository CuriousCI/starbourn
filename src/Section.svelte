<article
	class="{$$props.class}-article"
	id={$$props.id}
	style="background-image: url('../assets/compressed/{$$props.img}.jpg');"
>
	<section class={$$props.class}>
		<div>
			<h1>{@html $$props.title}</h1>
			<p><slot /></p>
		</div>
	</section>
</article>

<style>
	article {
		width: 100%;
		height: 100vh;

		background-position: center;
		background-size: cover;
		background-repeat: no-repeat;
		background-position-y: -20vh;

		display: flex;
		align-items: flex-end;
	}

	h1 {
		font-size: 48px;
	}

	p {
		font-size: 16px;
	}

	section {
		width: 100%;
		height: 40vh;

		display: grid;
		place-items: center;

		background: linear-gradient(
			0deg,
			rgba(0, 0, 0, 1) 50%,
			rgba(0, 0, 0, 0) 100%
		);
	}

	@media (min-width: 992px) {
		article {
			align-items: center;
			background-position: bottom;
		}

		.right-article {
			justify-content: flex-end;
		}

		h1 {
			font-size: 48px;
		}

		p {
			font-size: 16px;
		}

		section {
			width: 70vw;
			height: 100%;

			box-sizing: border-box;
		}

		.left {
			justify-content: flex-start;

			background: linear-gradient(
				90deg,
				rgba(0, 0, 0, 1) 50%,
				rgba(0, 0, 0, 0) 100%
			);

			padding-left: 5vw;
		}

		.right {
			width: 70vw;
			height: 100%;

			justify-content: flex-end;

			background: linear-gradient(
				270deg,
				rgba(0, 0, 0, 1) 50%,
				rgba(0, 0, 0, 0) 100%
			);

			box-sizing: border-box;
			padding-right: 5vw;
		}
	}

	@media (min-width: 1200px) {
		h1 {
			font-size: 100px;
		}
	}
</style>
