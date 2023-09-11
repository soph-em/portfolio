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
				projectDescription="Open Source contributions to calendar app supporting event scheduling for a community 50,000 strong. Migrated project architecture to React Router to enhance routing and navigation, added associated comprehensive testing suite, and proactively identified and resolved software defects via detailed bug reports. My contributions modernised the codebase, improved stability and performance, and enabled a smoother user experience for tens of thousands of users."
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
				projectDescription="Built an engaging daily browser game that challenges users to identify subreddits from images, utilizing SvelteKit, GitHub Actions, and a custom Python Reddit API wrapper. Programmatically accessed the Reddit API daily to draw from a vast image pool, automatically deploying new content at midnight using GitHub Actions for a dynamic user experience."
				technologies={['SvelteKit', 'Python', 'PRAW', 'GitHub Actions']}
			/>
		</div>

		<div class="project">
			<Project
				projectName="Space Raiders"
				projectimg="https://github.com/soph-em/soph-em/raw/main/images/spaceRaidersPico.gif"
				projectimgalt="video of 8bit space raiders"
				projectGithub="https://github.com/soph-em/pico8spaceraiderclone"
				projectDescription="Developed an immersive space combat game from the ground up using PICO-8, an innovative fantasy console and game engine. Programmed core gameplay logic, retro graphics, and sound effects using Lua to create a fully playable space shooter within the constraints of PICO-8's retro-styled virtual machine."
				technologies={['Pico8', 'Lua']}
			/>
		</div>

		<div class="project">
			<Project
				projectName="Photography Portfolio"
				projectimg="https://github.com/soph-em/soph-em/raw/main/images/Screencast-from-2023-07-17-16-57-29.gif"
				projectimgalt="video of photography portfolio website showing several landscape photos"
				projectGithub="https://github.com/soph-em/sophieearlphotography"
				projectLink="https://sophieearlphotography.pages.dev/"
				projectDescription="Created a custom photography portfolio website to showcase my work using SvelteKit for a streamlined, user-friendly experience. Combined my passion for photography with modern web development skills to build a lightweight, responsive platform. Taking advantage of SvelteKit's modular architecture to craft a fast, optimized site that loads seamlessly across devices. The end result is a sleek, efficient way to share my photography. "
				technologies={['Sveltekit']}
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
			<p>email: <a href="mailto:"> sophie@softwarecrab.com</a></p>
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
		background-color: #f0f8ff;
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
			display: flex;
			flex-direction: column;
			align-items: center; /* Center items horizontally */
			text-align: center; /* Center text within each project item */
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
			/* width: 75%; */
			/* margin: 0 auto; */
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
	@media screen and (min-width: 320px) and (max-width: 639px) {
		.contactlinks {
			flex-direction: column;
		}
		img {
			max-width: 100%;
		}
		.pfp {
			height: auto;
		}
	}
</style>
