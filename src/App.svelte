<svelte:options />

<script>
	import Header from './Header.svelte';
	import Contact from './Contact.svelte';

	const sections = [
		{
			title: 'Our Story',
			paragraph:
				'StarBourn Studios Is A Media Company That Offers 360-Degree Media Solutions We Produce Content For TV Shows, Films, Digital And Offer Unique Brand Solutions',
			image: '2',
			align: 'left',
		},
		{
			title: 'Development & Production',
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
				'We Provide Entertainment Marketing Services To Forward Thinking Brands',
			image: '8',
			align: 'left',
		},
	];

	let scrolling = false;
	let y;
	let menu;

	$: scrolling = y >= 50;
	$: menu = Math.floor(y / window.innerHeight);
</script>

<svelte:window bind:scrollY={y} />

<main>
	<Header
		bind:scrolling
		bind:menu
		menus={[
			'Home',
			'Starbourn',
			...sections.map((section) => section.title),
			'Get in Touch',
		]}
	/>

	<div
		id="Home"
		class="window cover home"
		style="background-image: url(assets/compressed/1.jpg);"
	>
		<h1 class="title">
			We bring ideas to life!<br />Stories to entertain<br />the audience
			around the world
		</h1>

		<h4>
			"Storytelling is the most powerful way to put ideas into the world
			today." --Robert McKee
		</h4>
	</div>

	<iframe
		id="Starbourn"
		class="window"
		src="https://www.youtube.com/embed/F5UPc8dya-M?controls=0"
		title="YouTube video player"
		frameborder="0"
		allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
		allowfullscreen
	/>

	{#each sections as section}
		<div
			id={section.title}
			class="window cover section {section.align}"
			style="background-image: url(assets/compressed/{section.image}.jpg);"
		>
			<div>
				<h1>{section.title}</h1>
				<p>{section.paragraph}</p>
			</div>
		</div>
	{/each}

	<Contact>
	</Contact>

	<footer>
		<p>footer</p>
	</footer>
</main>

<style>

	.contacts {
		display: flex;
		flex-direction: column;
	}

	.home {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: space-around;
		background-color: white;
	}

	.left {
		justify-content: flex-start;
	}

	.right {
		justify-content: flex-end;
	}

	.section {
		display: flex;
		align-items: center;
		box-sizing: border-box;
		padding: 0 200px;
	}

	.title {
		text-align: center;
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
