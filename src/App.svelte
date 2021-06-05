<script>
	import Header from './Header.svelte';

	const sections = [
		{
			title: 'Our Story',
			paragraph:
				'StarBourn Studios Is A Media Company That Offers 360-Degree Media Solutions We Produce Content For TV Shows, Films, Digital And Offer Unique Brand Solutions',
			image: '2',
			align: 'left',
		},
		{
			title: 'Development \n& Production',
			paragraph:
				'TV Formats\nFactual/ Non-Scripted\nFeature Films\nShort Films\nDocumentary\nDigital - OTT',
			image: '3',
			align: 'right',
		},
		{
			title: 'Discover Us',
			paragraph:
				'Content Creation\nVideo Production\nPost Production\nCommercial\nCorporate\nPrint & Digital',
			image: '4',
			align: 'left',
		},
		{
			title: 'Imagine Beyond',
			paragraph:
				'Creative - Ideation & Planning\nContent Production & Creation\nDistribution & Marketing',
			image: '5',
			align: 'right',
		},
		{
			title: 'Branding',
			paragraph:
				'We Provide Entertainment Marketing\nServices To Forward Thinking Brands',
			image: '6',
			align: 'left',
		},
	];
</script>

<main>
	<Header />

	<!-- <video controls>
		<source src="" type="video" /> -->

	<!-- width="1280" height="720" -->
	<!-- allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" -->
	<iframe
		src="https://www.youtube.com/embed/F5UPc8dya-M?controls=0&autoplay=1"
		title="YouTube video player"
		frameborder="0"
		allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
		allowfullscreen
	/>
	<!-- Not supported
	</video> -->

	{#each sections as section}
		<div
			class="section {section.align}"
			style="background-image: url(assets/{section.image}.jpg);"
		>
			<div>
				<h1>{section.title}</h1>
				<p>{section.paragraph}</p>
			</div>
		</div>
	{/each}
</main>

<style>
	iframe {
		position: relative;
		width: 100%;
		height: 100vh;
	}

	.left {
		justify-content: flex-start;
	}

	.right {
		justify-content: flex-end;
	}

	.section {
		position: relative;
		width: 100%;
		height: 100vh;

		display: flex;
		align-items: center;
		box-sizing: border-box;
		padding: 0 200px;

		background-position: center;
		background-size: cover;
	}

	h1 {
		font-size: 100px;
	}

	p {
		font-size: 27px;
	}

	h1,
	p {
		white-space: pre-line;
	}
</style>
