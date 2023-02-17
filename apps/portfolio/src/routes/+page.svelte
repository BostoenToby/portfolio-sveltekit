<script lang="ts">
	const languages = [
		'HTML5',
		'CSS3',
		'Javascript',
		'Typescript',
		'TailwindCSS',
		'Svelte',
		'VueJS',
		'React',
		'C#',
		'Python',
		'MySQL',
	]
</script>

<style scoped>
	.container {
		gap: 6rem;
		flex: 1 1 auto;
	}

	.information {
		flex-direction: column;
	}

	.title {
		font-size: 2rem;
		color: var(--green);
		padding-bottom: 2rem;
	}

	.subtitle {
		font-size: 1.5rem;
		color: var(--text);
	}

	.image {
		display: block;
		width: auto;
		height: auto;
		max-width: 30vw;
		border-radius: 15px;
	}

	.grid-lang {
		padding-top: 2rem;
		display: grid;
		grid-template-columns: repeat(4, 1fr);
		gap: 1rem;
	}

	.container-lang {
		flex-direction: column;
		padding: 1rem;
		background-color: var(--gray);
		border-radius: 5px;
		color: var(--text);
	}

	.icon {
		font-size: 1.5rem;
		color: var(--green);
		padding-bottom: 0.5rem;
	}

	@media only screen and (max-width: 1024px) {
		.container {
			display: flex;
			flex-direction: column;
			gap: 2rem;
		}

		.image {
			max-width: 50vw;
			margin-bottom: 2rem;
		}

		.information {
			margin-top: 2rem;
		}
	}

	@media only screen and (max-width: 640px) {
		.grid-lang {
			grid-template-columns: repeat(3, 1fr);
		}

		.title {
			font-size: 2rem;
		}

		.subtitle {
			font-size: 1rem;
		}

		.container-lang {
			padding: 8px;
		}
	}

	@media only screen and (max-width: 450px) {
		.grid-lang {
			grid-template-columns: repeat(2, 1fr);
		}
	}
</style>

<svelte:head>
  <title>Home</title>
  <meta name="description" content="Home of Bostoen Toby's portfolio" />
  <link rel="canonical" href="https://tobybostoen.be" />
</svelte:head>

<main class="container center">
	<section class="information center">
		<h1 class="title">Bostoen Toby</h1>
		<h2 class="subtitle">Full-stack Web Developer</h2>
		<h3 class="subtitle">based in Belgium</h3>
		<div class="grid-lang">
			{#each languages as language}
				{#if language != 'C#'}
					<div class="container-lang center">
						<i class="devicon-{language.toLocaleLowerCase()}-plain icon" />
						<!-- <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/{language}/{language}-plain.svg" alt="{language} icon" loading="lazy"> -->
						<p>{language}</p>
					</div>
				{:else}
					<div class="container-lang center">
						<i class="devicon-csharp-plain icon" />
						<!-- <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/csharp/csharp-plain.svg" alt="Csharp icon" loading="lazy"> -->
						<p>{language}</p>
					</div>
				{/if}
			{/each}
		</div>
	</section>

	<img
		height="2179"
		width="2136"
		class="image"
		src="/personalimage.webp"
		alt="Bostoen Toby smiling to the camera" />

</main>
