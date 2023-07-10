<script lang="ts">
	import logo from '../routes/logo.svg';
	import Project from './project.svelte';
</script>

<section>
	<img src={logo} alt="logo" />
</section>

<section class="page">
	<div class="projects">
		<h2>Projects</h2>
		<Project
			projectName="Subreddit Guesser"
			projectimg="https://github.com/soph-em/soph-em/raw/main/images/subredditGuesser.gif"
			projectimgalt="video of subreddit guesser website"
			projectGithub="https://github.com/soph-em"
			projectLink="https://subredditguesser.com/"
			projectDescription="Browser game with daily challenge to guess what subreddit an image was posted in. Updates at midnight daily using GitHub Actions."
			technologies={['SvelteKit', 'Python', 'PRAW', 'GitHub Actions']}
		/>
	</div>
</section>

<!-- logo colour #005286; -->
<style>
	.page {
		background-color: aliceblue;
	}
	.projects {
		margin: auto;

		width: 50%;

		padding: 10px;
		/* height: 1000px; */
	}
	section {
		/* height: 100vh; */
		width: 100%;
		/* background-color: black; */
		text-align: center;
	}
	img {
		height: 80vh;
		width: auto;
		max-width: 100%;
	}

	@media screen and (max-width: 640px) {
		.projects {
			padding: 0;
			width: 100%;
			padding-top: 20px;
		}
		img {
			height: 50vh;
		}
		section {
			height: 50vh;
			width: auto;
		}
	}
	@media screen and (min-width: 640px) and (max-width: 1280px) {
		.projects {
			margin: auto;

			width: 50%;

			padding: 10px;
		}
		section {
			height: fit-content;
		}
	}
</style>
