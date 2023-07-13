<script lang="ts">
	import { formatDate } from '../../lib/utils';
	import * as config from '../../lib/config';

	export let data;
</script>

<svelte:head>
	<title>{config.title}</title>
</svelte:head>

<!-- Posts -->
<section>
	<ul class="posts">
		{#each data.posts as post}
			<li class="post">
				<a href={post.slug} class="title">{post.title}</a>
				<p class="date">{formatDate(post.date)}</p>
				<p class="description">{post.description}</p>
			</li>
		{/each}
	</ul>
</section>

<!-- <script lang="ts">
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
</style> -->

<!-- <style>
	.posts {
		display: grid;
		gap: 2rem;
	}

	.post {
		max-inline-size: var(--size-content-3);
	}

	.post:not(:last-child) {
		border-bottom: 1px solid var(--border);
		padding-bottom: var(--size-7);
	}

	.title {
		font-size: var(--font-size-fluid-3);
		text-transform: capitalize;
	}

	.date {
		color: var(--text-2);
	}

	.description {
		margin-top: var(--size-3);
	}
</style> -->
