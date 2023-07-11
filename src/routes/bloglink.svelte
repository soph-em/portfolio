<script>
	export let photo;
	export let photoalt;
	export let title;
	export let description;
	export let date;
	export let pfp;
	export let link;
</script>

<div class="content">
	<a href={link}>
		<img src={photo} alt={photoalt} />
		<h2>{title}</h2>
		<p>{description}</p>
		<div class="author">
			<img class="pfp" src={pfp} alt="Sophie Earl " />
			<div class="me">
				<p class="name">Sophie Earl</p>
				<p class="date">{date}</p>
			</div>
		</div>
	</a>
</div>

<style>
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
		justify-content: center;
		padding-top: 50px;
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
