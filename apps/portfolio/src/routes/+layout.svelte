<script lang="ts">
	import '@fontsource/montserrat'
	import { Sun, Home, Cpu, Contact, Download } from 'lucide-svelte'
</script>

<style scoped>
	:root {
		--green: #339989;
		--gray: #e2e8f0;
	}

	:global(body, html) {
		height: 100%;
		margin: 0;
		font-family: 'Montserrat', sans-serif;
	}

	a {
		text-decoration: none;
		color: black;
	}

	:global(h1, h2, h3, h4, h5, h6, p) {
		margin: 0;
		padding: 0;
	}

	.page {
		display: flex;
		flex-direction: column;
		height: 100%;
	}

	.header {
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding: 1rem 1.5rem;
	}

	.title {
		font-size: 1rem;
		color: var(--green);
		padding-bottom: 6px;
		border-bottom: 3px solid var(--green);
		cursor: pointer;
	}

	.nav {
		display: flex;
		justify-content: space-between;
		align-items: center;
		gap: 4rem;
	}

	.container-right {
		display: flex;
		align-items: center;
		gap: 2rem;
	}

	.sun-container {
		border: none;
		background-color: inherit;
		color: var(--green);
		cursor: pointer;
	}

	.contact {
		font-size: 1rem;
		padding: 1rem;
		background-color: var(--gray);
		border: none;
		border-radius: 5px;
		cursor: pointer;
	}

	.contact:hover {
		box-shadow: 2px 2px 10px var(--gray);
	}

	.container {
		display: flex;
		flex: 1 1 auto;
	}

	.footer {
		position: sticky;
		bottom: 0;
		width: 100%;
		height: 80px;
		border-top: solid 1px var(--gray);
		background-color: white;
	}

	.footer-container {
		height: 100%;
		margin: auto;
		display: flex;
		width: 80%;
		justify-content: space-between;
	}

	.navigation-bottom {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		gap: 0.5rem;
		padding: 8px 0;
	}

	.navigation-top:hover {
		color: var(--green);
		padding-bottom: 4px;
	}

	@media only screen and (max-width: 1024px) {
		.header {
			display: none;
		}
	}

	@media only screen and (min-width: 1024px) {
		.footer {
			display: none;
		}
	}
</style>

<main class="page">
	<header class="header">
		<a href="/" class="title">Bostoen Toby</a>
		<nav class="nav">
			<a href="/" class="navigation-top">Home</a>
			<a href="/projects" class="navigation-top">Projects</a>
			<a href="/about" class="navigation-top">About</a>
			<a
				href="/cv.pdf"
				target="_blank"
				rel="noopener noreferrer"
				class="navigation-top">
				CV
			</a>
		</nav>
		<div class="container-right">
			<button class="sun-container">
				<Sun class="sun" />
			</button>
			<button class="contact">Contact</button>
		</div>
	</header>
	<slot class="container" />
	<footer class="footer">
		<nav class="footer-container">
			<a href="/" class="navigation-bottom">
				<Home />
				<p>Home</p>
			</a>
			<a href="/projects" class="navigation-bottom">
				<Cpu />
				<p>Projects</p>
			</a>
			<a href="/about" class="navigation-bottom">
				<Contact />
				<p>About</p>
			</a>
			<a
				href="/cv.pdf"
				target="_blank"
				rel="noopener norefferer"
				class="navigation-bottom">
				<Download />
				<p>CV</p>
			</a>
		</nav>
	</footer>
</main>
