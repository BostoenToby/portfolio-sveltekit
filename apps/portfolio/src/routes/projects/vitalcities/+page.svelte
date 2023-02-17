<script lang="ts">
	import { ArrowLeft } from 'lucide-svelte'

	const tags = [
		'Gatsby',
		'Netlify',
		'CMS',
		'Typescript',
		'GraphQL',
		'TailwindCSS',
		'Google Sheets API',
	]
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

	@media only screen and (max-width: 768px) {
		.container-tags {
			grid-template-columns: repeat(2, 1fr);
		}
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
</style>

<main class="container">
	<a href="/projects" class="back">
		<ArrowLeft />
		<p>All projects</p>
	</a>
	<section class="between information-head">
		<div class="container-information">
			<a href="https://beweegscan.vitalcities.be" class="title">
				Vital Cities Beweegscan
			</a>
			<p class="information-text">
				A big project I've made with a team of 5 people was a website for Vital
				Cities. This was in my second year of my bachelor course Multimedia and
				Creative Technologies. The customer wanted an online tool where people
				could compare their city with other cities on certain aspects. These
				aspects go from the amount of green spaces and benches to criminality
				scores for all cities. The main goal is let people know that there are
				better ways of transport than the car like public transportation,
				cycling, ...
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
		src="/vitalcities-1.webp"
		alt="Home of Vital Cities Beweegscan" />
	<div class="explanation-container">
		<p class="information-text">
			The challenge with this website was that the customer wanted to be able to
			add certain articles and change some aspects of the site in the future. The
			data that is used to compare cities with eachother also needed to be
			updatable every four years so that data has been put into a Google Sheets
			file. This file is then accessed with the Google Sheets API and processed
			with GraphQL. When the user wants a report on his city compared to the
			average city, he can easily give in his name, lastname, city and e-mail
			address and a mail will be sent with a PDF of the metrics. All the ambitions
			Vital Cities stands for are visualized with images, some explanation and
			usefull information but also with relevant articles for the people who want
			to know more.
		</p>
	</div >
</main>
