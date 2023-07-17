<script lang="ts">
	import Footer from './footer.svelte';
	import Navbar from './navbar.svelte';
	import Testnavbar from './testnavbar.svelte';
	import '../app.css';
</script>

<div>
	<Navbar />
	<slot />
	<Footer />
</div>

<style>
	:global(body) {
		margin: 0;
	}
	:global(p, h1, h2, h3) {
		font-family: 'Montserrat', sans-serif;
	}
	:global(html) {
		scroll-behavior: smooth;
		background-color: aliceblue;
	}
</style>
