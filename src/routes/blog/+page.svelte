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
		<a href={post.slug}>
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
		</a>
	{/each}
</div>

<style>
	img {
		max-height: 40vh;
		max-width: 30vw;
	}
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
		/* padding-bottom: 50px; */
	}
	.content {
		display: flex;
		flex-direction: column;
		padding-top: 90px;
		/* min-height: 90vh; */
		align-items: center;
		justify-content: center;
		margin: auto;
		text-align: center;
	}
	.author {
		display: flex;
		text-align: center;
		/* width: 20%; */
		align-items: center;
		justify-content: center;
		margin: auto;
		padding-bottom: 30px;
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
