<script lang="ts">
	interface ExperienceItem {
		company: string;
		position: string;
		duration: string;
		location: string;
		description: string;
		achievements: string[];
		technologies: string[];
	}

	// Sample data - replace with your actual work experience
	const experiences: ExperienceItem[] =[
	{
		"company": "Stockbit",
		"position": "Lead Backend Engineer",
		"duration": "Dec 2024 - Present",
		"location": "Surabaya, Indonesia",
		"description": "Lead the Account team, managing backend services and APIs for Sekuritas account creation and maintenance.",
		"achievements": [
			"Led 8 backend engineers in creating a secure, scalable and high-performance Sekuritas Account System",
			"Managed, Scaled and Improved Sekuritas Account System that handles over 7000+ daily Sekuritas Account creations, with total of 2 millions users, from integrating with KSEI, CFA creation with multiple major Banks in Indonesia, to Integration with downstream services such as Transaction and Settlement",
			"Building engineering culture where Testing and Integrity are integral to our processes, by introducing various engineering practice like TDD, Trunk Based Development and Shift-Left Testing",
			"Developed a robust KYC Platform, reducing registration/onboard friction while maintaining regulatory standards",
			"Collaborate with Web, Apps, Quality engineers in delivering multiple projects such as: Mandiri Bank Integration, Multi Porto and IFA SubAccount System, and AWS Migration",
			"Spearheaded the backend architecture for Sekuritas account lifecycle, from creation to verification, improving success rate and user satisfaction"
		],
		"technologies": ["Go", "gRPC", "PostgreSQL", "PubSub", "Kafka", "MySQL", "Redis"]
	},
	{
		"company": "GovTech Edu (INA Digital)",
		"position": "Software Architect",
		"duration": "Jul 2023 - Dec 2024",
		"location": "Surabaya, Indonesia",
		"description": "Designed and implemented scalable microservices architecture for Indonesia's government education platform.",
		"achievements": [
			"Delivered services supporting 300k+ schools with fast and reliable access to the national report card system",
			"Enabled 500k+ teachers and headmasters with comprehensive digital tools for education management",
			"Led Rapor IAM Migration to achieve a granular, scalable, and maintainable Identity and Access Management system",
			"Mentored junior developers and conducted code reviews to uphold best practices"
		],
		"technologies": ["Go", "gRPC", "PostgreSQL", "PubSub", "Redis"]
	},
	{
		"company": "GovTech Edu (INA Digital)",
		"position": "Senior Software Engineer",
		"duration": "Jul 2022 - Jun 2023",
		"location": "Surabaya, Indonesia",
		"description": "Developed and enhanced core services for Indonesia's national education platform, modernizing legacy systems and improving operational efficiency.",
		"achievements": [
			"Implemented an accurate and reliable report card system for 300k+ schools in Indonesia",
			"Implemented an accurate and reliable report card system for 500k+ students in Indonesia",
			"Collaborated with Data Engineer, Data Analyst, Product and UI/UX in preparing comprehensive documentation and training materials for our Users"
		],
		"technologies": ["Go", "gRPC", "PostgreSQL", "PubSub", "Redis"]
	},
	{
		"company": "Bukalapak",
		"position": "Tech Lead - Core & Trust Team",
		"duration": "Sep 2021 - Jun 2022",
		"location": "Jakarta, Indonesia",
		"description": "Led the Core & Trust engineering team to maintain and improve critical backend services ensuring platform integrity and user safety.",
		"achievements": [
			"Guided a cross-functional team in delivering high-availability, mission-critical services",
			"Enhanced fraud detection systems and trust-related features to protect millions of users",
			"Implemented technical strategies to improve service scalability and fault tolerance"
		],
		"technologies": ["Go", "PostgreSQL", "Kafka", "Redis", "Ruby on Rails", "MySQL"]
	},
	{
		"company": "Bukalapak",
		"position": "Software Development Engineer II",
		"duration": "Jan 2021 - Jun 2022",
		"location": "Jakarta, Indonesia",
		"description": "Focused on modernizing transaction and invoice systems to improve performance, scalability, and maintainability.",
		"achievements": [
			"Migrated legacy invoice services to a scalable microservices architecture",
			"Redesigned invoice generation process to improve speed and reduce operational errors",
			"Collaborated with multiple teams to ensure seamless integration across various vertical business"
		],
		"technologies": ["Go", "PostgreSQL", "Kafka", "Redis", "Ruby on Rails", "MySQL"]
	},
	{
		"company": "Bukalapak",
		"position": "Software Development Engineer I",
		"duration": "Jul 2019 - Dec 2020",
		"location": "Jakarta, Indonesia",
		"description": "Worked on enhancing and maintaining the shopping experience in the Bukalapak Marketplace.",
		"achievements": [
			"Developed and optimized core shopping features to improve user engagement and conversion",
			"Collaborated with product teams to deliver new features aligned with business goals",
			"Handle integration with Coupon, Voucher, Cart, and Product to deliver a fast, reliable and enticing Product Page Information"
		],
		"technologies": ["Go", "PostgreSQL", "Kafka", "Redis", "Ruby on Rails", "MySQL"]
	},
	{
		"company": "Renseki",
		"position": "Backend Developer",
		"duration": "Dec 2017 - Jun 2019",
		"location": "Surabaya, Indonesia",
		"description": "Developed various ERP-based web projects, tailoring solutions to client-specific business needs.",
		"achievements": [
			"Designed and implemented backend modules for inventory, sales, stock and finance",
			"Improved system performance through query optimization and caching",
			"Worked closely with clients to gather requirements and deliver custom ERP features"
		],
		"technologies": ["Java", "Spring", "MySQL", "Vaadin"]
	}];
</script>

<section class="section">
	<h2>Work Experience</h2>
	
	<div class="experience-list">
		{#each experiences as exp, index}
			<div class="experience-item">
				<div class="experience-header">
					<div class="job-info">
						<h3>{exp.position}</h3>
						<p class="company">{exp.company} • {exp.location}</p>
					</div>
					<div class="duration">
						<span class="duration-badge">{exp.duration}</span>
					</div>
				</div>
				
				<p class="description">{exp.description}</p>
				
				<div class="achievements">
					<h4>Key Achievements:</h4>
					<ul>
						{#each exp.achievements as achievement}
							<li>{achievement}</li>
						{/each}
					</ul>
				</div>
				
				<div class="technologies">
					<span class="tech-label">Technologies:</span>
					{#each exp.technologies as tech, techIndex}
						<span class="tech-tag">{tech}</span>
					{/each}
				</div>
			</div>
		{/each}
	</div>
</section>

<style>
	.experience-list {
		display: flex;
		flex-direction: column;
		gap: 2.5rem;
	}

	.experience-item {
		position: relative;
		padding-left: 1.5rem;
		border-left: 3px solid #64748b;
	}

	.experience-item::before {
		content: "";
		position: absolute;
		left: -6px;
		top: 0;
		width: 12px;
		height: 12px;
		background-color: #60a5fa;
		border-radius: 50%;
	}

	.experience-header {
		display: flex;
		justify-content: space-between;
		align-items: flex-start;
		margin-bottom: 1rem;
		gap: 1rem;
	}

	.job-info h3 {
		margin-bottom: 0.25rem;
	}

	.company {
		color: #94a3b8 !important;
		font-weight: 500;
		margin-bottom: 0 !important;
	}

	.duration-badge {
		background-color: #1e40af;
		color: #dbeafe;
		padding: 0.25rem 0.75rem;
		border-radius: 1rem;
		font-size: 0.875rem;
		font-weight: 500;
		white-space: nowrap;
	}

	.description {
		margin-bottom: 1.5rem;
		font-style: italic;
	}

	.achievements h4 {
		font-size: 1rem;
		font-weight: 600;
		margin-bottom: 0.75rem;
		color: #e2e8f0;
	}

	.achievements ul {
		margin-bottom: 1.5rem;
	}

	.technologies {
		display: flex;
		flex-wrap: wrap;
		align-items: center;
		gap: 0.5rem;
	}

	.tech-label {
		font-weight: 600;
		color: #e2e8f0;
	}

	.tech-tag {
		background-color: #64748b;
		color: #f1f5f9;
		padding: 0.25rem 0.5rem;
		border-radius: 0.375rem;
		font-size: 0.875rem;
		font-weight: 500;
	}

	@media (max-width: 768px) {
		.experience-header {
			flex-direction: column;
			gap: 0.5rem;
		}

		.duration-badge {
			align-self: flex-start;
		}

		.technologies {
			flex-direction: column;
			align-items: flex-start;
		}
	}
</style>
