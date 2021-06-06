<svelte:options />

<script>
	import Header from './Header.svelte';

	const sections = [
		{
			title: 'Our Story',
			paragraph:
				'StarBourn Studios Is A Media Company That Offers 360-Degree Media Solutions We Produce Content For TV Shows, Films, Digital And Offer Unique Brand Solutions',
			image: '2-min',
			align: 'left',
		},
		{
			title: 'Development & Production',
			paragraph:
				'TV Formats\nFactual/ Non-Scripted\nFeature Films\nShort Films\nDocumentary\nDigital - OTT',
			image: '3-min',
			align: 'right',
		},
		{
			title: 'Discover Us',
			paragraph:
				'Content Creation\nVideo Production\nPost Production\nCommercial\nCorporate\nPrint & Digital',
			image: '4-min',
			align: 'left',
		},
		{
			title: 'Imagine Beyond',
			paragraph:
				'Creative - Ideation & Planning\nContent Production & Creation\nDistribution & Marketing',
			image: '5-min',
			align: 'right',
		},
		{
			title: 'Branding',
			paragraph:
				'We Provide Entertainment Marketing Services To Forward Thinking Brands',
			image: '8-min',
			align: 'left',
		},
	];

	let scrolling = false;
	let y;

	$: scrolling = y >= 50;
</script>

<svelte:window bind:scrollY={y} style="scroll-behavior: smooth;" />

<main>
	<Header
		bind:scrolling
		menus={[
			'Home',
			...sections.map((section) => section.title),
			'Get in Touch',
		]}
	/>

	<div
		id="Home"
		class="window cover home"
		style="background-image: url(assets/resized-compressed-image/1-min.jpg);"
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
	<!-- &autoplay=1 -->
	<iframe
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
			style="background-image: url(assets/resized-compressed-image/{section.image}.jpg);"
		>
			<div>
				<h1>{section.title}</h1>
				<p>{section.paragraph}</p>
			</div>
		</div>
	{/each}

	<div id="Get in Touch" class="window contacts">
		<h1>Get in Touch</h1>
		<p>Let the magic begin</p>
		<form on:submit|preventDefault>
			<input type="text" placeholder="Name" />
			<input type="text" placeholder="Phone Number" />
			<input type="mail" placeholder="Email" />
			<textarea
				placeholder="Type your message here"
				cols="30"
				rows="10"
			/>
			<input type="submit" />
		</form>
	</div>

	<footer>
		<p>footer</p>
	</footer>
</main>

<style>
	form {
		display: flex;
		flex-direction: column;
		width: 40%;
	}

	.contacts {
		display: flex;
		flex-direction: column;
	}

	.home {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: space-around;
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
