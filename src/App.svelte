<script>
	import Header from './Header.svelte';
	import Home from './sections/Home.svelte';
	import Storylab from './sections/Storylab.svelte';
	import Footer from './Footer.svelte';
	import Contacts from './sections/Contacts.svelte';
	import Section from './Section.svelte';

	let scrollY = 0;
</script>

<svelte:window bind:scrollY />

<main>
	<Header
		bind:scrollY
		menus={[
			'home',
			'storylab',
			'story',
			'development',
			'discover',
			'beyond',
			'branding',
			'contacts',
		]}
	/>

	<Home />
	<Storylab />
	<Section class="left" title="Our Story" id="story" img="2">
		StarBourn Studios Is A Media Company That<br />
		Offers 360-Degree Media Solutions<br />
		We Produce Content For TV Shows, Films,<br />
		Digital And Offer Unique Brand Solutions
	</Section>
	<Section
		class="right"
		title="Development &<br />Production"
		id="development"
		img="3"
	>
		TV Formats<br />
		Factual/ Non-Scripted<br />
		Feature Films<br />
		Short Films<br />
		Documentary<br />
		Digital - OTT
	</Section>
	<Section class="left" title="Discover Us" id="discover" img="4">
		Content Creation<br />
		Video Production<br />
		Post Production<br />
		Commercial<br />
		Corporate<br />
		Print & Digital
	</Section>
	<Section class="right" title="Imagine Beyond" id="beyond" img="5">
		Creative - Ideation & Planning<br />
		Content Production & Creation<br />
		Distribution & Marketing
	</Section>
	<Section class="left" title="Branding" id="branding" img="8">
		We Provide Entertainment Marketing<br />
		Services To Forward Thinking Brands
	</Section>
	<Contacts />
	<Footer />
</main>
