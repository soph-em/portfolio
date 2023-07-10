<script lang="ts">
</script>

<nav>
	<h2>
		<h2 class="logo">Sophie Earl</h2>
	</h2>
	<button class="burger">
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
			><path
				d="M4,10h24c1.104,0,2-0.896,2-2s-0.896-2-2-2H4C2.896,6,2,6.896,2,8S2.896,10,4,10z M28,14H4c-1.104,0-2,0.896-2,2 s0.896,2,2,2h24c1.104,0,2-0.896,2-2S29.104,14,28,14z M28,22H4c-1.104,0-2,0.896-2,2s0.896,2,2,2h24c1.104,0,2-0.896,2-2 S29.104,22,28,22z"
				fill="black"
			/></svg
		>
	</button>
	<div class="collapse">
		<h2>
			<a href="/">Home</a>
		</h2>
		<h2>
			<a href="/#projects">My Work</a>
		</h2>
		<!-- <h2>
		<a href="/expertise">Expertise</a>
	</h2> -->
		<h2>
			<a href="/blog">Blog</a>
		</h2>
		<h2>
			<a href="/contact">Contact</a>
		</h2>
	</div>
</nav>

<!-- 
<style>
	h2 {
		padding-left: 10%;
		padding-right: 10%;
		color: white;
		width: fit-content;
		text-align: center;
		min-width: 100px;
		max-height: 50px;
		font-size: smaller;
	}
	nav {
		height: 50px;
		background-color: black;
		display: flex;
		flex-direction: row;
	}
	ul {
		list-style-type: none;
		margin: 0;
		padding: 0;
		overflow: hidden;
		background-color: black;
	}

	li {
		float: left;
	}

	li a {
		display: block;
		color: white;
		text-align: center;
		padding: 16px;
		text-decoration: none;
	}

	li a:hover {
		background-color: #333333;
	}
</style> -->

<style>
	.burger {
		display: none;
	}
	a {
		display: block;
		color: aliceblue;
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
			font-size: xx-small;
		}
		.logo {
			padding: 0;
		}
	}

	@media screen and (max-width: 660px) {
		.burger {
			display: flex;
			margin-right: 20px;
		}

		nav {
			max-width: 100vw;
		}

		h2 {
			font-size: small;
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
