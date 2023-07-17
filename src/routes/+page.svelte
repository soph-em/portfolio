<script lang="ts">
	import logo from '../routes/logo.svg';
	import Project from './project.svelte';
	import pfp from './pfp.jpg';
</script>

<section class="hero">
	<img src={logo} alt="logo" />
</section>

<section class="page contact">
	<div class="projects" id="projects">
		<h2>My Work</h2>
		<div class="project">
			<Project
				projectName="Together"
				projectimg="https://github.com/soph-em/soph-em/raw/main/images/together.gif"
				projectimgalt="video of Together Calendar website"
				projectGithub="https://github.com/Together-100Devs/Together"
				projectLink="https://together.cyclic.app/"
				projectDescription="Open Source contributions to calendar app supporting event scheduling for a community 40,000 strong. Added a component, converted project to react-router and added associated testing, submitted bug report."
				technologies={['React', 'Tailwind CSS', 'Node.JS', 'Express.JS', 'MongoDB', 'Cypress']}
			/>
		</div>
		<div class="project">
			<Project
				projectName="Subreddit Guesser"
				projectimg="https://github.com/soph-em/soph-em/raw/main/images/subredditGuesser.gif"
				projectimgalt="video of subreddit guesser website"
				projectGithub="https://github.com/soph-em/subredditguesser"
				projectLink="https://subredditguesser.com/"
				projectDescription="Browser game with daily challenge to guess what subreddit an image was posted in. Uses Python Reddit API Wrapper to access Reddit API/Images. Updates at midnight daily using GitHub Actions."
				technologies={['SvelteKit', 'Python', 'PRAW', 'GitHub Actions']}
			/>
		</div>

		<div class="project">
			<Project
				projectName="Space Raiders"
				projectimg="https://github.com/soph-em/soph-em/raw/main/images/spaceRaidersPico.gif"
				projectimgalt="video of 8bit space raiders"
				projectGithub="https://github.com/soph-em/pico8spaceraiderclone"
				projectDescription="Space raiders game made in PICO-8 virtual machine and game engine/Lua-based environment."
				technologies={['Pico8', 'Lua']}
			/>
		</div>
	</div>
</section>

<section class="contact" id="contact">
	<h2>Contact</h2>
	<p>
		I am open to freelance or employment opportunities. To speak to me or arrange a freelance
		consultation please get in contact via either social media or email.
	</p>
	<div class="contactlinks">
		<img class="pfp" src={pfp} alt="Sophie Earl" />
		<div class="links">
			<p>email: <a href="mailto:"> ***to be added***</a></p>
			<p>
				twitter: <a target="_blank" href="https://twitter.com/soph_m_e">@soph_m_e</a>
			</p>
			<p>
				github: <a target="_blank" href="https://github.com/soph-em">soph-em</a>
			</p>
		</div>
	</div>
</section>

<style>
	.project {
		padding-top: 2rem;
	}
	.contact {
		width: 50%;
		padding-bottom: 3%;
	}
	.links {
		flex-direction: column;
		padding-left: 1rem;
	}
	.contactlinks {
		display: flex;
		text-align: center;
		width: 60%;
		align-items: center;
		justify-content: center;
		margin: auto;
	}
	.pfp {
		height: 10rem;
		border-radius: 50%;
	}
	p {
		max-width: 80vw;
		text-align: center;
	}
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

	section {
		text-align: center;
		margin: auto;
		padding: 10px;
	}
	img {
		height: 100%;
		max-width: 100%;
	}

	@media screen and (max-width: 640px) {
		.projects {
			padding: 0;
			width: 100%;
		}
		img {
			height: 50%;
		}
		section {
			height: 50%;
		}
		.hero {
			padding-top: 20%;
			height: 40%;
		}
		.contact {
			width: 75%;
		}
	}
	@media screen and (min-width: 640px) and (max-width: 1280px) {
		.projects {
			margin: auto;
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
