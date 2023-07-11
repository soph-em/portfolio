<script lang="ts">
	import Bloglink from '../bloglink.svelte';
	// import post from '../blog/pico8/day1_Llama';
	import llama1 from '../blog/pico8/day1_Llama/Screenshot from 2023-07-11 21-19-11.png';
</script>

<section>
	<Bloglink
		title="Pico8 llama game - Day 1"
		description="Day one of me making a small pico8 llama game!"
		photo={llama1}
		photoalt="pico8 game"
		date="7th July 2023"
		pfp="https://avatars.githubusercontent.com/u/92051936?v=4"
		link="/blog/pico8/day1_Llama"
	/>
</section>

<style>
	section {
		padding-top: 50px;
		/* height: 90vh; */
		width: 100%;
		/* background-color: black; */
		text-align: center;
	}
</style>
