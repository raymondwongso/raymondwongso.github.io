<script lang="ts">
	// Sample data - replace with your actual about information
	const aboutText = `
		Software Engineer with 8+ years of experience designing and building scalable web applications and distributed systems. Skilled in delivering product-focused software on modern web servers, cloud-native architectures, and leveraging agile methodologies to drive business value. Passionate about creating reliable, high-performance solutions that scale with user needs.
	`;

	const highlights = [
		"8+ years of professional experience in software development, delivering scalable and high-quality solutions",
        "3+ years in leadership and management roles, guiding teams to success",
		"Expertise in Go, PostgreSQL and Cloud technologies (GCP and AWS)",
		"Proven track record in microservices architecture and distributed system design",
		"Advocate for clean code, best practices, and continuous improvement",
        "AI-powered workstation and productivity tools enthusiast"
	];
</script>

<section class="section">
	<h2>About</h2>
	<p class="about-description">{aboutText}</p>
	
	<div class="highlights">
		<h3>Key Highlights</h3>
		<ul>
			{#each highlights as highlight}
				<li>{highlight}</li>
			{/each}
		</ul>
	</div>
</section>

<style>
	.about-description {
		font-size: 1.1rem;
		line-height: 1.7;
		margin-bottom: 2rem;
	}

	.highlights h3 {
		margin-bottom: 1rem;
		color: #374151;
	}

	.highlights ul {
		list-style-type: none;
		padding-left: 0;
	}

	.highlights li {
		position: relative;
		padding-left: 1.5rem;
		margin-bottom: 0.5rem;
	}

	.highlights li::before {
		content: "✓";
		position: absolute;
		left: 0;
		color: #10b981;
		font-weight: bold;
	}
</style>
