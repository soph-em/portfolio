<script lang="ts">
	import { formatDate } from '../../lib/utils';
	import * as config from '../../lib/config';

	export let data;
</script>

<svelte:head>
	<title>{config.title}</title>
</svelte:head>
<div class="content">
	{#each data.posts as post}
		<img src={post.headerimage} />
		<h2><a href={post.slug} class="title">{post.title}</a></h2>
		<p>{post.description}</p>
		<div class="author">
			<img class="pfp" src={post.author} alt="Sophie Earl " />
			<div class="me">
				<p class="name">Sophie Earl</p>
				<p class="date">{formatDate(post.date)}</p>
			</div>
		</div>
	{/each}
</div>

<style>
	p {
		padding: 0;
		margin-top: 0;
	}
	a {
		text-decoration: none;
		color: inherit;
		outline: 0;
		/* cursor: auto; */
	}
	.me {
		padding-left: 20px;
	}
	.content {
		display: flex;
		flex-direction: column;
		padding-top: 90px;
		/* min-height: 90vh; */
		align-items: center;
		justify-content: center;
		margin: auto;
	}
	.author {
		display: flex;
		text-align: center;
		width: 20%;
		align-items: center;
		justify-content: center;
		margin: auto;
	}
	.pfp {
		border-radius: 50%;
		height: 50px;
	}
	.date {
		font-size: smaller;
		margin: 0;
	}
	.name {
		margin: 0;
	}
	@media screen and (max-width: 660px) {
		.author {
			width: 50%;
		}
		img {
			max-width: 350px;
		}
	}
</style>
