<script>
	import Header from './Header.svelte';
	import Home from './sections/Home.svelte';
	import Storylab from './sections/Storylab.svelte';
	import Story from './sections/Story.svelte';
	import Development from './sections/Development.svelte';
	import Discover from './sections/Discover.svelte';
	import Beyond from './sections/Beyond.svelte';
	import Branding from './sections/Branding.svelte';
	import Footer from './Footer.svelte';
	import Contacts from './sections/Contacts.svelte';

	let scrollY;
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
	<Story />
	<Development />
	<Discover />
	<Beyond />
	<Branding />
	<Contacts />
	<Footer />
</main>
