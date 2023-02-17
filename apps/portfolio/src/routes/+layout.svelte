<script lang="ts">
	import '@fontsource/montserrat'
	import { Sun, Home, Cpu, Contact, Download } from 'lucide-svelte'

	const changeTheme = () => {
		if (
			window.document.documentElement.style.getPropertyValue('--background') ===
			'#FFFFFF'
		) {
			window.document.documentElement.style.setProperty(
				'--background',
				'#1f2937',
			)
			window.document.documentElement.style.setProperty('--green', '#7DE2D1')
			window.document.documentElement.style.setProperty('--green-x-dark', '#7DE2D1')
			window.document.documentElement.style.setProperty('--gray', '#334155')
			window.document.documentElement.style.setProperty('--text', '#FFFFFF')
		} else {
			window.document.documentElement.style.setProperty(
				'--background',
				'#FFFFFF',
			)
			window.document.documentElement.style.setProperty('--green', '#339989')
			window.document.documentElement.style.setProperty('--green-x-dark', '#246157')
			window.document.documentElement.style.setProperty('--gray', '#e2e8f0')
			window.document.documentElement.style.setProperty('--text', '#000000')
		}
	}
</script>

<style scoped>
	:root {
		--background: #ffffff;
		--green-x-dark: #246157;
		--green: #339989;
		--gray: #e2e8f0;
		--text: #000000;
	}

	:global(body, html) {
		height: 100%;
		margin: 0;
		font-family: 'Montserrat', sans-serif;
		background-color: var(--background);
	}

	a {
		text-decoration: none;
		color: black;
	}

	:global(h1, h2, h3, h4, h5, h6, p) {
		margin: 0;
		padding: 0;
	}

	:global(.center) {
		display: flex;
		justify-content: center;
		align-items: center;
	}

	:global(.between) {
		display: flex;
		justify-content: space-between;
		align-items: center;
	}

	.page {
		display: flex;
		flex-direction: column;
		height: 100%;
	}

	.header {
		padding: 1rem 1.5rem;
	}

	.title {
		font-size: 1rem;
		color: var(--green-x-dark);
		padding-bottom: 6px;
		border-bottom: 3px solid var(--green-x-dark);
		cursor: pointer;
	}

	.nav {
		gap: 4rem;
	}

	.container-right {
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

	.contact-text {
		color: var(--text);
	}

	.container {
		display: flex;
		flex: 1 1 auto;
	}

	.footer-nav {
		position: sticky;
		bottom: 0;
		width: 100%;
		height: 80px;
		border-top: solid 1px var(--gray);
		background-color: var(--background);
	}

	.footer-container {
		height: 100%;
		margin: auto;
		width: 80%;
	}

	.footer-information {
		margin: 1rem 8rem;
	}

	.footer-title {
		font-size: 1rem;
		color: var(--text);
	}

	.container-links {
		display: flex;
		align-items: center;
		gap: 2rem;
	}

	.navigation-bottom {
		flex-direction: column;
		gap: 0.5rem;
		padding: 8px 0;
		color: var(--text);
	}

	.navigation-top {
		color: var(--text);
	}

	.navigation-top:hover {
		color: var(--green);
		padding-bottom: 4px;
	}

	.link {
		color: var(--text);
	}

	.link:hover {
		color: var(--green);
		text-decoration: underline;
	}

	.hidden {
		display: none;
	}

	@media only screen and (max-width: 1024px) {
		.nav {
			display: none;
		}

		.footer-information {
			margin: 1rem 2rem;
		}
	}

	@media only screen and (min-width: 1024px) {
		.footer-nav {
			display: none;
		}
	}
</style>

<main class="page">
	<header class="header between">
		<a href="/" class="title">Bostoen Toby</a>
		<nav class="nav between">
			<a href="/" class="navigation-top">Home</a>
			<a href="/projects" class="navigation-top">Projects</a>
			<a href="/about" class="navigation-top">About</a>
			<a
				href="/CV.pdf"
				target="_blank"
				rel="noopener noreferrer"
				class="navigation-top">
				CV
			</a>
		</nav>
		<div class="container-right center">
			<button on:click={changeTheme} class="sun-container">
				<Sun class="sun" />
				<p class="hidden">Change theme</p>
			</button>
			<button class="contact">
				<a href="mailto:toby.bostoen123@gmail.com" class="contact-text">Contact</a>
			</button>
		</div>
	</header>
	<slot class="container" />
	<footer>
		<section class="footer-information between">
			<p class="footer-title">© 2023 Bostoen Toby</p>
			<div class="container-links">
				<a href="https://www.linkedin.com/in/toby-bostoen/" class="link">
					LinkedIn
				</a>
				<a href="https://github.com/BostoenToby" class="link">Github</a>
				<a href="mailto:toby.bostoen123@gmail.com" class="link">Mail</a>
			</div>
		</section>
	</footer>
	<nav class="footer-nav">
		<div class="footer-container between">
			<a href="/" class="navigation-bottom center">
				<Home />
				<p>Home</p>
			</a>
			<a href="/projects" class="navigation-bottom center">
				<Cpu />
				<p>Projects</p>
			</a>
			<a href="/about" class="navigation-bottom center">
				<Contact />
				<p>About</p>
			</a>
			<a
				href="/CV.pdf"
				target="_blank"
				rel="noopener norefferer"
				class="navigation-bottom center">
				<Download />
				<p>CV</p>
			</a>
		</div>
	</nav>
</main>
