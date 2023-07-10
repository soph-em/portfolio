<script lang="ts">
</script>

<nav>
	<h2>
		<h2 class="logo">Sophie Earl</h2>
	</h2>
	<h2>
		<a href="/">Home</a>
	</h2>
	<h2>
		<a href="/">My Work</a>
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

	@media screen and (max-width: 950px) {
		nav {
			max-width: 100vw;
		}

		h2 {
			font-size: small;
		}
		.logo {
			padding: 0;
		}
	}
</style>
