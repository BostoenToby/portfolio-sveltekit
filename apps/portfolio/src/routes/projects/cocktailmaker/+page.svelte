<script lang="ts">
	const tags = ['Raspberry Pi', 'Python', 'Electronics', 'HTML5', 'CSS3']
</script>

<style scoped>
	.container {
		flex: 1 1 auto;
		margin: 0 8rem;
	}

	.back {
		display: flex;
		align-items: center;
		gap: 1rem;
		font-size: 1.5rem;
		text-decoration: none;
		color: var(--text);
		width: fit-content;
		cursor: pointer;
	}

	.back:hover {
		color: var(--green);
	}

	.container-information {
		max-width: 60%;
	}

	.container-tags {
		display: grid;
		grid-template-columns: repeat(3, 1fr);
		gap: 1rem;
	}

	.information-head {
		margin: 2rem 0 3rem;
		gap: 4rem;
	}

	.title {
		font-size: 2rem;
		color: var(--green);
		text-align: left;
	}

	.information-text {
		font-size: 1rem;
		line-height: 1.8rem;
		margin: 2rem 0 1rem;
		color: var(--text);
		max-width: 90%;
	}

	.tag {
		padding: 0.5rem 1rem;
		border-radius: 5px;
		background-color: var(--green);
		color: white;
		font-size: 1rem;
	}

	.container-img {
		display: block;
		width: auto;
		height: auto;
		max-width: 80vw;
		border-radius: 15px;
		margin: 0 auto 4rem;
	}

	.explanation-container {
		max-width: 90%;
		margin: auto;
	}

	@media only screen and (max-width: 1024px) {
		.back {
			margin: 4rem 0;
			width: max-content;
		}

		.title {
			width: max-content;
		}

		.information-head {
			flex-direction: column;
		}

		.container-information {
			max-width: 90%;
			margin: auto;
		}

		.container {
			margin: 0 1rem;
		}

		.container-tags {
			grid-template-columns: repeat(3, 1fr);
		}
	}

	@media only screen and (max-width: 640px) {
		.container-tags {
			grid-template-columns: repeat(2, 1fr);
		}
	}
</style>

<svelte:head>
	<title>Project Cocktail Maker</title>
	<meta
		name="description"
		content="The Cocktail Maker project from Bostoen Toby" />
	<link rel="canonical" href="https://tobybostoen.be/projects/cocktailmaker" />
</svelte:head>

<main class="container">
	<a href="/projects" class="back">
		<img src="/arrow-left.svg" alt="Arrow left icon" />
		<p>All projects</p>
	</a>
	<section class="information-head between">
		<div class="container-information">
			<h1 class="title">Cocktail Maker</h1>
			<p class="information-text">
				My first ever project was a cocktailmaker made with a Raspberry Pi and
				with an interface online. At the end of my first year Bachelor
				Multimedia and Creative Technologies we needed to make a project with
				the Raspberry Pi and some sensors. The summer was coming so it looked
				like a fun idea to make a cocktailmaker where you can put your own
				ingredients in the back and let the machine make you a cocktail.
			</p>
		</div>
		<div class="container-tags">
			{#each tags as tag}
				<div class="tag center">
					<p>{tag}</p>
				</div>
			{/each}
		</div>
	</section>
	<img
		class="container-img"
		height="890"
		width="1890"
		src="/cocktailmaker-1.webp"
		alt="Casing of the Cocktail maker" />
	<div class="explanation-container">
		<p class="information-text">
			This was the first time I've worked on a project alone of this size. Some
			struggles I've had were the pumps to pump the liquid to the cup because
			some needed to be submitted in the liquid and that wasn't possible. After
			some time searching I did come across pumps that could pump up the liquid
			without being submerged but there was liquid leaking when it was pumping.
			I can assure you that liquid and electronics aren't the best combination,
			but I've managed to keep the leaking to a minimum and it worked out in the
			end. On the display there are cocktails displayed that can be ordered, but
			also an IP-address that you can go to. On this website you could see how
			many times a certain cocktail was ordered and how much of the drinks in
			the back are left. There would also be a message when the drinks were
			almost empty so you could put in new bottles. I've learned a lot during
			the making of the Cocktail Maker on the technical side, but also on how to
			plan certain things so you don't run into problems later on.
		</p>
	</div>
</main>
