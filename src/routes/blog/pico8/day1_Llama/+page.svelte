<script lang="ts">
	import Post from '../../../blogpost.svelte';
	import llama from '../day1_Llama/Screenshot from 2023-07-11 21-19-11.png';
</script>

<section>
	<Post
		title="Pico8 Llama Game - Day 1"
		content={['Read about my first day']}
		photo={llama}
		photoalt="pico8 game"
		date="7th July 2023"
		pfp="https://avatars.githubusercontent.com/u/92051936?v=4"
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
