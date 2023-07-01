<script>
	// @ts-nocheck

	import '../app.css';
	import Footer from '../components/footer.svelte';
	import Header from '../components/header.svelte';
	import PageTransition from '../components/transition.svelte';

	export let data;
</script>

<Header />
<main>
	<PageTransition url={data.url}>
		<slot />
	</PageTransition>
</main>
<Footer />
