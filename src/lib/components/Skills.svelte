<script lang="ts">
	interface SkillCategory {
		category: string;
		skills: {
			name: string;
			level: 'Beginner' | 'Intermediate' | 'Advanced' | 'Expert';
		}[];
	}

	// Sample data - replace with your actual skills
	const skillCategories: SkillCategory[] = [
		{
			category: "Programming Languages",
			skills: [
				{ name: "Go", level: "Expert" },
				{ name: "Ruby", level: "Advanced" },
				{ name: "Java", level: "Advanced" },
				{ name: "C#", level: "Intermediate" },
				{ name: "Rust", level: "Beginner" }
			]
		},
		{
			category: "Databases & Caching",
			skills: [
				{ name: "PostgreSQL", level: "Expert" },
				{ name: "MySQL", level: "Expert" },
				{ name: "Redis", level: "Expert" },
				{ name: "Elasticsearch", level: "Advanced" },
				{ name: "MongoDB", level: "Advanced" }
			]
		},
		{
			category: "Event Source Platform",
			skills: [
				{ name: "Kafka", level: "Expert" },
				{ name: "RedPanda", level: "Expert" },
				{ name: "Google PubSub", level: "Expert" },
			]
		},
		{
			category: "Cloud & DevOps",
			skills: [
				{ name: "GCP", level: "Expert" },
				{ name: "Docker", level: "Expert" },
				{ name: "AWS", level: "Advanced" },
				{ name: "Kubernetes", level: "Intermediate" },
				{ name: "Terraform", level: "Intermediate" }
			]
		},
		{
			category: "Tools & Others",
			skills: [
				{ name: "Git", level: "Expert" },
				{ name: "System Architecture", level: "Expert" },
				{ name: "Linux", level: "Advanced" },
				{ name: "Trunk Based Development", level: "Advanced" },
				{ name: "Agile/Scrum", level: "Advanced" }
			]
		}
	];

	function getLevelColor(level: string): string {
		switch (level) {
			case 'Expert': return '#10b981';
			case 'Advanced': return '#3b82f6';
			case 'Intermediate': return '#f59e0b';
			case 'Beginner': return '#ef4444';
			default: return '#6b7280';
		}
	}

	function getLevelWidth(level: string): string {
		switch (level) {
			case 'Expert': return '100%';
			case 'Advanced': return '80%';
			case 'Intermediate': return '60%';
			case 'Beginner': return '40%';
			default: return '0%';
		}
	}
</script>

<section class="section">
	<h2>Technical Skills</h2>
	
	<div class="skills-grid">
		{#each skillCategories as category}
			<div class="skill-category">
				<h3>{category.category}</h3>
				<div class="skills-list">
					{#each category.skills as skill}
						<div class="skill-item">
							<div class="skill-header">
								<span class="skill-name">{skill.name}</span>
								<span class="skill-level" style="color: {getLevelColor(skill.level)}">{skill.level}</span>
							</div>
							<div class="skill-bar">
								<div 
									class="skill-progress" 
									style="width: {getLevelWidth(skill.level)}; background-color: {getLevelColor(skill.level)}"
								></div>
							</div>
						</div>
					{/each}
				</div>
			</div>
		{/each}
	</div>
</section>

<style>
	.skills-grid {
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
		gap: 2rem;
	}

	.skill-category {
		background-color: #475569;
		border: 1px solid #64748b;
		border-radius: 0.75rem;
		padding: 1.5rem;
	}

	.skill-category h3 {
		margin-bottom: 1.5rem;
		color: #f8fafc;
		text-align: center;
	}

	.skills-list {
		display: flex;
		flex-direction: column;
		gap: 1rem;
	}

	.skill-item {
		display: flex;
		flex-direction: column;
		gap: 0.5rem;
	}

	.skill-header {
		display: flex;
		justify-content: space-between;
		align-items: center;
	}

	.skill-name {
		font-weight: 500;
		color: #e2e8f0;
	}

	.skill-level {
		font-size: 0.875rem;
		font-weight: 600;
	}

	.skill-bar {
		height: 6px;
		background-color: #64748b;
		border-radius: 3px;
		overflow: hidden;
	}

	.skill-progress {
		height: 100%;
		border-radius: 3px;
		transition: width 0.3s ease;
	}

	@media (max-width: 1024px) {
		.skills-grid {
			grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
		}
	}
</style>
