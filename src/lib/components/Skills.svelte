<script lang="ts">
		interface SkillCategory {
			category: string;
			skills: string[];
		}

	// Sample data - replace with your actual skills
	const skillCategories: SkillCategory[] = [
	       {
		       category: "Programming Languages",
		       skills: ["Go", "Ruby", "Java", "C#", "Rust"]
	       },
	       {
		       category: "Databases & Caching",
		       skills: ["PostgreSQL", "MySQL", "Redis", "Elasticsearch", "MongoDB"]
	       },
	       {
		       category: "Event Source Platform",
		       skills: ["Kafka", "RedPanda", "Google PubSub"]
	       },
	       {
		       category: "Cloud & DevOps",
		       skills: ["GCP", "Docker", "AWS", "Kubernetes", "Terraform"]
	       },
	       {
		       category: "Tools & Others",
		       skills: ["Git", "System Architecture", "Linux", "Trunk Based Development", "Agile/Scrum"]
	       }
	];


</script>

<section class="section">
	<h2>Technical Skills</h2>
	
	<div class="skills-grid">
		{#each skillCategories as category}
			<div class="skill-category">
				<h3>{category.category}</h3>
		       <ul class="skills-list">
			       {#each category.skills as skill}
				       <li class="skill-name">{skill}</li>
			       {/each}
		       </ul>
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
	       list-style: disc inside;
	       margin: 0;
	       padding: 0;
	       display: flex;
	       flex-direction: column;
	       gap: 0.5rem;
       }

       .skill-name {
	       font-weight: 500;
	       color: #e2e8f0;
       }

	@media (max-width: 1024px) {
		.skills-grid {
			grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
		}
	}
</style>
