<script lang="ts">
	interface Project {
		name: string;
		description: string;
		technologies: string[];
		highlights: string[];
		githubUrl?: string;
		liveUrl?: string;
		imageUrl?: string;
	}

	// Sample data - replace with your actual projects
	const projects: Project[] = [
		{
			name: "E-Commerce Platform",
			description: "Full-stack e-commerce application with user authentication, payment processing, and admin dashboard.",
			technologies: ["React", "Node.js", "MongoDB", "Stripe", "AWS"],
			highlights: [
				"Implemented secure payment processing with Stripe",
				"Built responsive design with mobile-first approach",
				"Integrated real-time inventory management",
				"Deployed on AWS with auto-scaling capabilities"
			],
			githubUrl: "https://github.com/yourusername/ecommerce-platform",
			liveUrl: "https://your-ecommerce-demo.com"
		},
		{
			name: "Task Management App",
			description: "Collaborative task management application with real-time updates and team collaboration features.",
			technologies: ["Vue.js", "Express.js", "PostgreSQL", "Socket.io", "Docker"],
			highlights: [
				"Real-time collaboration using WebSockets",
				"Drag-and-drop task management interface",
				"Role-based access control",
				"Dockerized for easy deployment"
			],
			githubUrl: "https://github.com/yourusername/task-manager",
			liveUrl: "https://your-task-manager-demo.com"
		},
		{
			name: "Data Visualization Dashboard",
			description: "Interactive dashboard for visualizing complex datasets with customizable charts and filters.",
			technologies: ["React", "D3.js", "Python", "Flask", "Redis"],
			highlights: [
				"Interactive charts with D3.js",
				"Real-time data processing pipeline",
				"Customizable dashboard layouts",
				"Exported reports in multiple formats"
			],
			githubUrl: "https://github.com/yourusername/data-dashboard"
		},
		{
			name: "Mobile Weather App",
			description: "Cross-platform mobile application for weather forecasting with location-based services.",
			technologies: ["React Native", "TypeScript", "Redux", "OpenWeather API"],
			highlights: [
				"Cross-platform compatibility (iOS/Android)",
				"Location-based weather forecasting",
				"Offline data caching",
				"Beautiful animations and transitions"
			],
			githubUrl: "https://github.com/yourusername/weather-app"
		}
	];
</script>

<section class="section">
	<h2>Featured Projects</h2>
	
	<div class="projects-grid">
		{#each projects as project}
			<div class="project-card">
				<div class="project-header">
					<h3>{project.name}</h3>
					<div class="project-links">
						{#if project.githubUrl}
							<a href={project.githubUrl} target="_blank" rel="noopener" class="link-button">
								<span class="icon">📁</span>
								Code
							</a>
						{/if}
						{#if project.liveUrl}
							<a href={project.liveUrl} target="_blank" rel="noopener" class="link-button">
								<span class="icon">🚀</span>
								Live Demo
							</a>
						{/if}
					</div>
				</div>
				
				<p class="project-description">{project.description}</p>
				
				<div class="project-highlights">
					<h4>Key Features:</h4>
					<ul>
						{#each project.highlights as highlight}
							<li>{highlight}</li>
						{/each}
					</ul>
				</div>
				
				<div class="project-technologies">
					{#each project.technologies as tech}
						<span class="tech-tag">{tech}</span>
					{/each}
				</div>
			</div>
		{/each}
	</div>
</section>

<style>
	.projects-grid {
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
		gap: 2rem;
	}

	.project-card {
		background-color: #475569;
		border: 1px solid #64748b;
		border-radius: 0.75rem;
		padding: 1.5rem;
		transition: transform 0.2s ease, box-shadow 0.2s ease;
	}

	.project-card:hover {
		transform: translateY(-2px);
		box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
	}

	.project-header {
		display: flex;
		justify-content: space-between;
		align-items: flex-start;
		margin-bottom: 1rem;
		gap: 1rem;
	}

	.project-header h3 {
		margin-bottom: 0;
	}

	.project-links {
		display: flex;
		gap: 0.5rem;
		flex-shrink: 0;
	}

	.link-button {
		display: flex;
		align-items: center;
		gap: 0.25rem;
		padding: 0.25rem 0.5rem;
		background-color: #60a5fa;
		color: white !important;
		border-radius: 0.375rem;
		font-size: 0.875rem;
		font-weight: 500;
		text-decoration: none;
		transition: background-color 0.2s ease;
	}

	.link-button:hover {
		background-color: #3b82f6;
		text-decoration: none;
	}

	.link-button .icon {
		font-size: 0.75rem;
	}

	.project-description {
		margin-bottom: 1.5rem;
		color: #cbd5e1;
	}

	.project-highlights h4 {
		font-size: 1rem;
		font-weight: 600;
		margin-bottom: 0.75rem;
		color: #e2e8f0;
	}

	.project-highlights ul {
		margin-bottom: 1.5rem;
		padding-left: 1rem;
	}

	.project-highlights li {
		font-size: 0.9rem;
		margin-bottom: 0.25rem;
	}

	.project-technologies {
		display: flex;
		flex-wrap: wrap;
		gap: 0.5rem;
	}

	.tech-tag {
		background-color: #1e40af;
		color: #dbeafe;
		padding: 0.25rem 0.5rem;
		border-radius: 0.375rem;
		font-size: 0.875rem;
		font-weight: 500;
	}

	@media (max-width: 1024px) {
		.projects-grid {
			grid-template-columns: 1fr;
		}

		.project-header {
			flex-direction: column;
			gap: 0.75rem;
		}

		.project-links {
			align-self: flex-start;
		}
	}
</style>
