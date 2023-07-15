<script lang="ts">
	import { formatDate } from '$lib/utils';

	export let data;
</script>

<!-- SEO -->
<svelte:head>
	<title>{data.meta.title}</title>
	<meta property="og:type" content="article" />
	<meta property="og:title" content={data.meta.title} />
</svelte:head>

<article class="content">
	<!-- Title -->
	<hgroup>
		<h2>{data.meta.title}</h2>

		<img class="header" src={data.meta.headerimage} />
		<div class="author">
			<img class="pfp" src={data.meta.author} />
			<div class="info">
				<p>Sophie Earl</p>
				<p class="date">Published at {formatDate(data.meta.date)}</p>
			</div>
		</div>
	</hgroup>

	<!-- Tags -->

	<!-- Post -->
	<div class="prose">
		<svelte:component this={data.content} />
	</div>
	<div class="tags">
		{#each data.meta.categories as category}
			<p class="surface-4">&num;{category}</p>
		{/each}
	</div>
</article>

<style>
	h2 {
		padding-top: 2rem;
	}
	p {
		margin: 5px;
	}
	.info {
		display: flex;
		flex-direction: column;
	}
	.author {
		display: flex;
		text-align: center;
		width: 40%;
		align-items: center;
		justify-content: center;
		margin: auto;
		padding-bottom: 1rem;
		padding-top: 1rem;
	}
	.header {
		max-height: 40vh;
		display: block;
		margin-inline: auto;
	}
	.pfp {
		max-height: 50px;
		border-radius: 50px;
	}
	article {
		max-inline-size: var(--size-content-3);
		margin-inline: auto;
		/* text-align: center; */
		padding-top: 10vh;
		max-width: 70vw;
		margin: auto;
	}

	.tags {
		display: flex;
		/* gap: var(--size-3);
		margin-top: var(--size-7); */
		text-align: center;
		display: flex;
		text-align: center;
		width: 20%;
		align-items: center;
		justify-content: center;
		margin: auto;
		/* margin: 10px; */
	}

	.tags > * {
		/* padding: var(--size-2) var(--size-3);
		border-radius: var(--radius-round); */
	}
</style>
