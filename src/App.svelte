<script>
	import Header from './Header.svelte';
	import Section from './Section.svelte';

	const sections = [
		{
			title: 'Our Story',
			paragraph:
				'StarBourn Studios Is A Media Company That Offers 360-Degree Media Solutions We Produce Content For TV Shows, Films, Digital And Offer Unique Brand Solutions',
			image: '',
		},
		{
			title: 'Development \n& Production',
			paragraph:
				'TV Formats\nFactual/ Non-Scripted\nFeature Films\nShort Films\nDocumentary\nDigital - OTT',
			image: '',
		},
		{
			title: 'Discover Us',
			paragraph:
				'Content Creation\nVideo Production\nPost Production\nCommercial\nCorporate\nPrint & Digital',
			image: '',
		},
		{
			title: 'Imagine Beyond',
			paragraph:
				'Creative - Ideation & Planning\nContent Production & Creation\nDistribution & Marketing',
			image: '',
		},
		{
			title: 'Branding',
			paragraph:
				'We Provide Entertainment Marketing Services To Forward Thinking Brands',
			image: '',
		},
	];
</script>

<main>
	<Header />
	{#each sections as section}
		<div class="section">
			<h1>{section.title}</h1>
			<p>{section.paragraph}</p>
			<img src="assets/{section.image}.jpg" alt="background" />
		</div>
	{/each}
</main>

<style>
	.section {
		position: relative;
		width: 100%;
		height: 100vh;
	}

	h1,
	p {
		white-space: pre-line;
	}
</style>
