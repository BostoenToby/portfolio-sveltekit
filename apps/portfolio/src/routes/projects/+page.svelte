<style scoped>
	.container {
		flex: 1 1 auto;
		margin: 0 8rem;
	}

	.space {
		display: flex;
		justify-content: space-between;
		align-items: center;
	}

	.button-information {
		padding: 2rem;
		margin: 4rem 0;
		cursor: pointer;
		text-decoration: none;
		border-radius: 15px;
	}

	.button-information:hover {
		background-color: var(--gray);
	}

	.image {
		max-width: 30%;
	}

	.information {
		max-width: 50%;
	}

	.project-title {
		color: var(--green);
		font-size: 1.5rem;
		text-align: start;
		margin-bottom: 24px;
	}

	.title {
		font-size: 2rem;
		color: var(--green);
		margin: 2rem 2rem 0;
	}

	.information-text {
		font-size: 1rem;
		line-height: 1.8rem;
		text-align: start;
		color: black;
	}

	@media only screen and (max-width: 1024px) {
		.project-container {
			display: grid;
			grid-template-columns: repeat(2, 1fr);
			gap: 2rem;
			margin-top: 4rem;
		}

		.project-container a {
			aspect-ratio: 1;
		}

		.information-text {
			display: none;
		}

		.button-information {
			margin: 0;
			display: flex;
			flex-direction: column-reverse;
			align-items: center;
			row-gap: 2rem;
			align-items: center;
			background-color: var(--gray);
		}

		.project-title {
			text-align: center;
			font-size: 1.5rem;
		}

		.information {
			max-width: 80%;
		}

		.image {
			max-width: 70%;
			max-height: 30%;
		}

		.space {
			flex-direction: column-reverse;
			align-items: center;
			justify-content: unset;
		}

		.title {
			margin: 2rem 0;
		}
	}
</style>

<svelte:head>
  <title>Projects</title>
  <meta name="description" content="Project from Bostoen Toby" />
  <link rel="canonical" href="https://tobybostoen.be/projects" />
</svelte:head>

<main class="container">
	<h1 class="title">Projects</h1>
	<section class="project-container">
		<a href="/projects/vitalcities" class="button-information space">
			<div class="information">
				<h2 class="project-title">Vital Cities Beweegscan</h2>
				<p class="information-text">
					A big project I've made with a team of 5 people was a website for
					Vital Cities. This was in my second year of my bachelor course
					Multimedia and Creative Technologies. The customer wanted an online
					tool where people could compare their city with other cities on
					certain aspects. These aspects go from the amount of green spaces and
					benches to criminality scores for all cities. The main goal is let
					people know that there are better ways of transport than the car like
					public transportation, cycling, ...
				</p>
			</div>
			<img
				src="/vitalcities.webp"
				alt="The logo of Vital Cities"
				class="image center" />
		</a>
		<a href="/projects/neohotel" class="button-information space">
			<div class="information">
				<h2 class="project-title">Neohotel</h2>
				<p class="information-text">
					This is a project I've made with a colleague in my last year of my
					bachelor course Multimedia and Creative Technologies as a exam for
					Advanced Full-Stack Web Development. The assignment was to create a
					full-stack website with real-time communication between front-end and
					back-end and multiple kinds of users. We chose for the hotel project
					which included a website for the customer to book his stay in the
					hotel, the possibility to get access to facilities and his room as
					well as a platform for the staff of the hotel.
				</p>
			</div>
			<img src="/neohotel.webp" alt="The logo of Neohotel" class="image" />
		</a>
		<a href="/projects/cocktailmaker" class="button-information space">
			<div class="information">
				<h2 class="project-title">Cocktail Maker</h2>
				<p class="information-text">
					My first ever project was a cocktailmaker made with a Raspberry Pi and
					with an interface online. At the end of my first year Bachelor
					Multimedia and Creative Technologies we needed to make a project with
					the Raspberry Pi and some sensors. The summer was coming so it looked
					like a fun idea to make a cocktailmaker where you can put your own
					ingredients in the back and let the machine make you a cocktail.
				</p>
			</div>
			<img
				src="/cocktailmaker.webp"
				alt="The logo of cocktailmaker"
				class="image" />
		</a>
	</section>
</main>
