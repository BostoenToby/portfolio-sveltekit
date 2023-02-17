<style scoped>
	.container {
		flex: 1 1 auto;
	}

	.container-information {
		padding: 2rem 8rem;
		margin: 8rem 0;
		gap: 2rem;
	}

	.information {
		max-width: 50%;
	}

	.image {
		max-width: 50%;
		border-radius: 15px;
		color: var(--text);
	}

	.title {
		font-size: 2rem;
		color: var(--green);
		text-align: left;
		margin-bottom: 24px;
	}

	.information-text {
		font-size: 1rem;
		line-height: 1.8rem;
		margin-bottom: 16px;
		color: var(--text);
	}

	@media only screen and (max-width: 1024px) {
		.container-information {
			padding: 0 0.5rem;
			margin: 2rem 0;
			flex-direction: column;
		}

		.container-information:nth-of-type(2) {
			flex-direction: column-reverse;
		}

		.title {
			font-size: 1.5rem;
		}

		.information {
			max-width: 90%;
			margin: auto;
		}
	}
</style>

<svelte:head>
  <title>About</title>
  <meta name="description" content="About Bostoen Toby" />
  <link rel="canonical" href="https://tobybostoen.be/about" />
</svelte:head>

<main class="container">
	<section class="between container-information">
		<div class="information">
			<h1 class="title">Some words about me</h1>
			<p class="information-text">
				I'm a passionate web developer mainly focused on front-end developing
				but also interested in the full-stack. As of today I'm a last year
				student at Howest Kortrijk in Belgium for a bachelor degree of
				Multimedia and Creative Technologies. Here we learn how to create web
				applications from start to finish. We learned what good UX and UI means
				in a application and how to actually program it. The front-end and
				back-end are both teached and some full-stack projects have already been
				made. We also learn to work with different frameworks and coding
				languages such as, for example: Svelte, Vue, NestJS, ...
			</p>
		</div>
		<img src="/laptop.webp" alt="Some words about me" class="image" />
	</section>
	<section class="between container-information">
		<img src="/work.webp" alt="Some of my qualities" class="image" />
		<div class="information">
			<h1 class="title">Some of my qualities</h1>
			<p class="information-text">
				In my time as a programmer I noticed that every time I see a structure
				or program, I try to understand how it works. Sometimes I even think of
				a way to make it more efficient or more accessible for the customer.
				Throughout my studies I stay open minded for new techniques and ways to
				make something work. Innovation is an important factor in programming to
				make sure the customer gets a top tier product.
			</p>
			<p class="information-text">
				Nobody is perfect as a human and my less good qualities are that I'm not
				always easily satisfied with a product. Sometimes an other design will
				fit better or there is a cleaner way to program something, but because
				of deadlines it's not always possible to optimize everything.
			</p>
		</div>
	</section>
	<section class="between container-information">
		<div class="information">
			<h1 class="title">Improve yourself</h1>
			<p class="information-text">
				In my free time I find it important to get a clear mind before working.
				It's the best way to start a productive day and have some optimal
				results. A morning walk can do such wonders to a person and you can make
				a planning for the day.
			</p>
			<p class="information-text">
				If there is one thing that became clear throughout my studies, it's that
				I want to start a company in my free time. It's an amazing feeling to
				make projects yourself fromm start to finish and to make a customer
				happy. I'm also open to collaborate on projects with other people. It
				would be awesome to get to know other developers and to realize new
				advanced application.
			</p>
		</div>
		<img src="/smile.webp" alt="Improve yourself" class="image" />
	</section>
</main>
