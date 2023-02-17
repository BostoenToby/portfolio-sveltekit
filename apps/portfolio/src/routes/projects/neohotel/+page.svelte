<script lang="ts">
	import { ArrowLeft } from 'lucide-svelte'

	const tags = [
		'Svelte',
		'NestJS',
		'Typescript',
		'GraphQL',
		'MongoDB',
		'TailwindCSS',
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

<svelte:head>
  <title>Project Neohotel</title>
  <meta name="description" content="The Neohotel project from Bostoen Toby" />
  <link rel="canonical" href="https://tobybostoen.be/projects/neohotel" />
</svelte:head>

<main class="container">
	<a href="/projects" class="back">
		<ArrowLeft />
		<p>All projects</p>
	</a>
	<section class="information-head between">
		<div class="container-information">
			<a href="https://neohotel.netlify.app/" class="title">Neohotel</a>
			<p class="information-text">
				This is a project I've made with a colleague in my last year of my
				bachelor course Multimedia and Creative Technologies as a exam for
				Advanced Full-Stack Web Development. The assignment was to create a
				full-stack website with real-time communication between front-end and
				back-end and multiple kinds of users. We chose for the hotel project
				which included a website for the customer to book his stay in the hotel,
				the possibility to get access to facilities and his room as well as a
				platform for the staff of the hotel.
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
		src="/neohotel-1.webp"
		alt="Home of Neohotel" />
	<div class="explanation-container">
		<p class="information-text">
			The challenge with this project was that throughout the lessons we learned
			new aspects like I18n, SocketIO, ... and we needed to implement these
			aspects into our own project. All these aspects were teached with the Vue
			framework so for a challenge we created the website in Svelte. At that
			time I had never used Svelte before and I immediately notices some
			problems like navigating. If you use Svelte (not Sveltekit), there is no
			standard navigator and to find one that is elegant is no easy task. Next
			to the assignment we implemented some other features like a 3D model of
			the rooms, Stripe for payment processing and also a QR-code that the user
			generates to enter the room. The QR-code that the user generates can be
			scanned and checked through a seperate application also made in Svelte.
			There was also testing implemented into the frontend with cypress as well
			as in the backend. The testing was then automated with Github actions
			every time we deployed or pushed to the repository.
		</p>
	</div>
</main>
