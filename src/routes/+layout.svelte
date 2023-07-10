<script lang="ts">
	import Navbar from './navbar.svelte';
	import Testnavbar from './testnavbar.svelte';
</script>

<!-- <Testnavbar /> -->
<Navbar />
<slot />

<style>
	:global(body) {
		margin: 0;
	}
	:global(p, h1, h2, h3) {
		font-family: 'Montserrat', sans-serif;
	}
	:global(html) {
		scroll-behavior: smooth;
	}
</style>
