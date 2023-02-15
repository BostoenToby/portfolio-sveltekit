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
		display: flex;
		justify-content: center;
		gap: 6rem;
		flex: 1 1 auto;
		align-items: center;
	}

	.information {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}

	.title {
		font-size: 3rem;
		color: var(--green);
		padding-bottom: 2rem;
	}

	.subtitle {
		font-size: 2rem;
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
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 1rem;
		background-color: var(--gray);
		border-radius: 5px;
	}

	.icon {
		font-size: 2rem;
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

<main class="container">
	<section class="information">
		<h1 class="title">Bostoen Toby</h1>
		<h2 class="subtitle">Full-stack Web Developer</h2>
		<h3 class="subtitle">based in Belgium</h3>
		<div class="grid-lang">
			{#each languages as language}
				{#if language != 'C#'}
					<div class="container-lang">
						<i class="devicon-{language.toLocaleLowerCase()}-plain icon" />
						<p>{language}</p>
					</div>
				{:else}
					<div class="container-lang">
						<i class="devicon-csharp-plain icon" />
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
		src="personalimage.jpg"
		alt="Bostoen Toby smiling to the camera" />

</main>
