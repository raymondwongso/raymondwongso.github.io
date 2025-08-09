<script lang="ts">
	import Header from '$lib/components/Header.svelte';
	import About from '$lib/components/About.svelte';
	import Experience from '$lib/components/Experience.svelte';
	import Skills from '$lib/components/Skills.svelte';
	import Education from '$lib/components/Education.svelte';
	import Contact from '$lib/components/Contact.svelte';
</script>

<svelte:head>
	<title>Raymond Wongso - Resume</title>
	<meta name="description" content="Professional resume and portfolio of Raymond Wongso" />
</svelte:head>

<main class="container">
	<div class="desktop-layout">
		<div class="left-column">
			<Header />
			<About />
			<Skills />
		</div>
		<div class="right-column">
			<Experience />
			<Education />
		</div>
	</div>
	
	<div class="mobile-layout">
		<Header />
		<About />
		<Experience />
		<Skills />
		<Education />
	</div>
</main>

<style>
	:global(*) {
		margin: 0;
		padding: 0;
		box-sizing: border-box;
	}

	:global(body) {
		font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
		line-height: 1.6;
		color: #e5e7eb;
		background-color: #0f172a;
		margin: 0;
		padding: 0;
	}

	.container {
		max-width: 1400px;
		margin: 0 auto;
		padding: 2rem 1rem;
		background-color: #1e293b;
		box-shadow: 0 0 20px rgba(0, 0, 0, 0.3);
		min-height: 100vh;
	}

	.desktop-layout {
		display: grid;
		grid-template-columns: 400px 1fr;
		gap: 3rem;
		align-items: start;
	}

	.mobile-layout {
		display: none;
	}

	.left-column {
		position: sticky;
		top: 2rem;
		background-color: #334155;
		border-radius: 1rem;
		padding: 2rem;
		box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
	}

	.right-column {
		background-color: #334155;
		border-radius: 1rem;
		padding: 2rem;
		box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
	}

	:global(h1) {
		font-size: 2.125rem;
		font-weight: 700;
		color: #f8fafc;
		margin-bottom: 0.5rem;
	}

	:global(h2) {
		font-size: 1.425rem;
		font-weight: 600;
		color: #3198ff;
		margin-bottom: 1rem;
		border-bottom: 2px solid #475569;
		padding-bottom: 0.5rem;
	}

	:global(h3) {
		font-size: 0.925rem;
		font-weight: 600;
		color: #f8fafc;
		margin-bottom: 0.5rem;
	}

	:global(p) {
		margin-bottom: 1rem;
		color: #cbd5e1;
	}

	:global(ul) {
		margin-bottom: 1rem;
		padding-left: 1.5rem;
	}

	:global(li) {
		margin-bottom: 0.3rem;
		color: #cbd5e1;
	}

	:global(a) {
		color: #60a5fa;
		text-decoration: none;
		transition: color 0.2s ease;
	}

	:global(a:hover) {
		color: #93c5fd;
		text-decoration: underline;
	}

	:global(.section) {
		margin-bottom: 2rem;
		padding: 1rem 0;
	}

	:global(.section:not(:last-child)) {
		border-bottom: 1px solid #475569;
	}

	@media (max-width: 1024px) {
		.desktop-layout {
			display: none;
		}

		.mobile-layout {
			display: block;
		}

		.mobile-layout > :global(.section) {
			background-color: #334155;
			border-radius: 1rem;
			padding: 2rem;
			margin-bottom: 2rem;
			box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
		}

		.container {
			padding: 1rem;
			margin: 0;
			box-shadow: none;
		}

		:global(h1) {
			font-size: 1.625rem;
		}

		:global(h2) {
			font-size: 1.125rem;
		}
	}
</style>
