<script>
	import Header from './Header.svelte';

	const sections = [
		{
			title: 'Our Story',
			paragraph:
				'StarBourn Studios Is A Media Company That Offers 360-Degree Media Solutions We Produce Content For TV Shows, Films, Digital And Offer Unique Brand Solutions',
			image: '1',
		},
		{
			title: 'Development \n& Production',
			paragraph:
				'TV Formats\nFactual/ Non-Scripted\nFeature Films\nShort Films\nDocumentary\nDigital - OTT',
			image: '2',
		},
		{
			title: 'Discover Us',
			paragraph:
				'Content Creation\nVideo Production\nPost Production\nCommercial\nCorporate\nPrint & Digital',
			image: '3',
		},
		{
			title: 'Imagine Beyond',
			paragraph:
				'Creative - Ideation & Planning\nContent Production & Creation\nDistribution & Marketing',
			image: '4',
		},
		{
			title: 'Branding',
			paragraph:
				'We Provide Entertainment Marketing Services To Forward Thinking Brands',
			image: '5',
		},
	];
</script>

<main>
	<Header />
	{#each sections as section}
		<div
			class="section"
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
	.section {
		position: relative;
		width: 100%;
		height: 100vh;

		display: flex;
		align-items: center;

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
