<script lang="ts">
	import logo from '../routes/logo.svg';
	import Project from './project.svelte';
</script>

<section class="hero">
	<img src={logo} alt="logo" />
</section>

<section class="page">
	<div class="projects" id="projects">
		<h2>My Work</h2>
		<Project
			projectName="Subreddit Guesser"
			projectimg="https://github.com/soph-em/soph-em/raw/main/images/subredditGuesser.gif"
			projectimgalt="video of subreddit guesser website"
			projectGithub="https://github.com/soph-em/subredditguesser"
			projectLink="https://subredditguesser.com/"
			projectDescription="Browser game with daily challenge to guess what subreddit an image was posted in. Updates at midnight daily using GitHub Actions."
			technologies={['SvelteKit', 'Python', 'PRAW', 'GitHub Actions']}
		/>
		<Project
			projectName="Together"
			projectimg="https://github.com/soph-em/soph-em/raw/main/images/together.gif"
			projectimgalt="video of Together Calendar website"
			projectGithub="https://github.com/Together-100Devs/Together"
			projectLink="https://together.cyclic.app/"
			projectDescription="Open Source contributions to calendar app supporting event scheduling for a community 40,000 strong. "
			technologies={['React', 'Tailwind CSS', 'Node.JS', 'Express.JS', 'MongoDB', 'Cypress']}
		/>
		<Project
			projectName="Space Raiders"
			projectimg="https://github.com/soph-em/soph-em/raw/main/images/spaceRaidersPico.gif"
			projectimgalt="video of 8bit space raiders"
			projectGithub="https://github.com/soph-em/pico8spaceraiderclone"
			projectDescription="Space raiders game made in Pico8/Lua-based environment."
			technologies={['Pico8', 'Lua']}
		/>
	</div>
</section>

<!-- logo colour #005286; -->
<style>
	h2 {
		color: #005286;
	}
	.hero {
		height: 80vh;
		padding-top: 10%;
	}
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
		/* height: 90vh; */
		width: 100%;
		/* background-color: black; */
		text-align: center;
	}
	img {
		height: 100%;
		/* width: auto; */
		max-width: 100%;
	}

	@media screen and (max-width: 640px) {
		.projects {
			padding: 0;
			width: 100%;
			/* padding-top: 50px; */
			/* height: fit-content; */
		}
		img {
			height: 50%;
		}
		section {
			height: 50%;
			width: auto;
		}
		.hero {
			padding-top: 20%;
			height: 40%;
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
		.hero {
			height: 40%;
		}
	}
</style>
