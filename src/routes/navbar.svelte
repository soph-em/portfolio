<script lang="ts">
	import twitter from '../routes/twitter-svgrepo-com.svg';
	import { onMount } from 'svelte';
	import { burgerMenuStore } from '../routes/burgerMenuStore';

	let isActive = false;

	function showMenu() {
		isActive = !isActive;
	}

	function closeMenu(event) {
		event.preventDefault();
		isActive = false;
		const href = event.target.getAttribute('href');

		setTimeout(() => {
			window.location.href = href;
		}, 300); // Adjust the delay as needed
	}

	onMount(() => {
		const showButton = document.getElementById('showButton');
		showButton.addEventListener('click', showMenu);

		return () => {
			showButton.removeEventListener('click', showMenu);
		};
	});

	$: {
		burgerMenuStore.set(isActive);
	}
</script>

<nav>
	<button class="burger" id="showButton">
		<svg
			style="color: white; background-colour: black"
			height="32px"
			id="Layer_1"
			version="1.1"
			viewBox="0 0 32 32"
			width="32px"
			xml:space="preserve"
			xmlns="http://www.w3.org/2000/svg"
			xmlns:xlink="http://www.w3.org/1999/xlink"
		>
			<path
				d="M4,10h24c1.104,0,2-0.896,2-2s-0.896-2-2-2H4C2.896,6,2,6.896,2,8S2.896,10,4,10z M28,14H4c-1.104,0-2,0.896-2,2 s0.896,2,2,2h24c1.104,0,2-0.896,2-2S29.104,14,28,14z M28,22H4c-1.104,0-2,0.896-2,2s0.896,2,2,2h24c1.104,0,2-0.896,2-2 S29.104,22,28,22z"
				fill="black"
			/>
		</svg>
	</button>
	<h2>
		<h2 class="logo">Sophie Earl</h2>
	</h2>
	<div class="collapse">
		<h2>
			<a href="/">Home</a>
		</h2>
		<h2>
			<a href="/#projects">My Work</a>
		</h2>
		<h2>
			<a href="/#contact">Contact</a>
		</h2>
		<!-- <h2>
	  <a href="/expertise">Expertise</a>
	</h2> -->
		<h2>
			<a href="/blog">Blog</a>
		</h2>
		<!-- <h2>
			<a href="https://twitter.com/soph_m_e" target="">My Twitter</a>
		</h2> -->
		<!-- <img src={twitter} /> -->
	</div>
</nav>

{#if isActive}
	<div class:active={$burgerMenuStore} class="burgerMenu">
		<h2>
			<a href="/" on:click={closeMenu}>Home</a>
		</h2>
		<h2>
			<a href="/#projects" on:click={closeMenu}>My Work</a>
		</h2>
		<h2>
			<a href="/#contact" on:click={closeMenu}>Contact</a>
		</h2>
		<!-- <h2>
      <a href="/expertise" on:click={closeMenu}>Expertise</a>
    </h2> -->
		<h2>
			<a href="/blog" on:click={closeMenu}>Blog</a>
		</h2>
	</div>
{/if}

<style>
	img {
		height: 25px;
		display: block;
		text-align: center;
		padding: 16px;
		text-decoration: none;
	}
	.burgerMenu {
		position: fixed;
		top: 0;
		left: 0;
		z-index: 9998;
		/* display: flex; */
		flex-direction: column;
		width: 40vw;
		height: 100vh;
		background-color: black;
		color: aliceblue;
		padding-top: 50px;
		justify-content: flex-end;
		transition: transform 0.5s ease-in-out, opacity 0.5s ease-in-out;
		transform: translateX(-100%);
		opacity: 0;
		padding-top: 90px;
		/* font-size: 48px; */
	}

	.burgerMenu.active {
		transform: translateX(0%);
		opacity: 1;
	}
	.burger {
		display: none;
		z-index: 9999;
		/* margin-left: 20px; */
		/* margin-right: 30px; */
	}

	a {
		color: aliceblue;
		display: block;
		text-align: center;
		padding: 16px;
		text-decoration: none;
		/* width: calc(100% - 32px);  */
	}

	nav {
		display: flex;
		flex-direction: row;
		width: 100%;
		justify-content: space-around;
		align-items: center;
		height: 4rem;
		background-color: black;
		position: fixed; /* Add this line */
		top: 0; /* Add this line */
		left: 0; /* Add this line */
		right: 0; /* Add this line */
		z-index: 9999;
	}

	h2 {
		font-family: 'Roboto Mono', monospace;
		font-size: medium;
		color: aliceblue;
		margin: 0;
		flex: 1;
	}

	.logo {
		align-self: centre;
		font-size: xx-large;
		padding-left: 10rem;
		padding-right: 5rem;
		white-space: nowrap;
	}

	a:hover {
		background-color: #333333;
	}

	.collapse {
		display: flex;
		flex-direction: row;
		width: 100%;
		justify-content: space-around;
		align-items: center;
		height: 4rem;
		background-color: black;
	}

	@media screen and (max-width: 500px) {
		nav {
			max-width: 100vw;
		}

		h2 {
			/* font-size: xx-small; */
		}

		.logo {
			padding: 0;
		}
	}

	@media screen and (max-width: 660px) {
		.burger {
			display: flex;
			margin-right: 40px;
		}

		nav {
			max-width: 100vw;
		}

		h2 {
			font-size: x-large;
			flex: 0;
		}

		.logo {
			padding: 0;
			padding-left: 2rem;
		}

		.collapse {
			display: none;
		}
	}

	@media screen and (max-width: 1200px) {
		.logo {
			padding: 0;
			padding-left: 2rem;
		}
	}
</style>
