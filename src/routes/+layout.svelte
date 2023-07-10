<script lang="ts">
	import Navbar from './navbar.svelte';
</script>

<Navbar />
<slot />

<style>
	:global(body) {
		margin: 0;
	}
	:global(p, h1, h2, h3) {
		font-family: 'Montserrat', sans-serif;
	}
</style>
