<script lang="ts">
	interface EducationItem {
		institution: string;
		degree: string;
		field: string;
		duration: string;
		location: string;
		gpa?: string;
		honors?: string[];
		relevantCourses?: string[];
	}

	interface CertificationItem {
		name: string;
		issuer: string;
		date: string;
		credentialId?: string;
		validUntil?: string;
	}

	// Education information
	const education: EducationItem[] = [
		{
			institution: "Institute Sains Terapan dan Teknologi Surabaya (iSTTS)",
			degree: "Bachelor",
			field: "Computer Software Engineering",
			duration: "2013 - 2017",
			location: "Surabaya, Indonesia",
			gpa: "3.51/4.0"
		}
	];

	// Certifications
	const certifications: CertificationItem[] = [
		{
			name: "Architecting with Google Kubernetes Engine: Foundations",
			issuer: "Google Cloud",
			date: "2022",
			credentialId: "KQQSH9BCQ4JU"
		},
		{
			name: "Elastic Google Cloud Infrastructure: Scaling and Automation",
			issuer: "Google Cloud",
			date: "2022",
			credentialId: "XKE58NP5TGRL"
		},
		{
			name: "Essential Google Cloud Infrastructure: Core Services",
			issuer: "Google Cloud",
			date: "2022",
			credentialId: "9PZ8FA9BPX8F"
		},
		{
			name: "Essential Google Cloud Infrastructure: Foundation",
			issuer: "Google Cloud",
			date: "2022",
			credentialId: "9TCF33LKVPL4"
		},
		{
			name: "Preparing for Google Cloud Certification: Cloud Engineer",
			issuer: "Google Cloud",
			date: "2022",
			credentialId: "MH2WS76KYUD6"
		},
		{
			name: "Google Cloud Fundamentals: Core Infrastructure",
			issuer: "Google Cloud",
			date: "2022",
			credentialId: "NAUVS4YA3AWL"
		}
	];
</script>

<section class="section">
	<h2>Education & Certifications</h2>
	
	<div class="education-section">
		<h3 class="subsection-title">Education</h3>
		<div class="education-list">
			{#each education as edu}
				<div class="education-item">
					<div class="education-header">
						<div class="education-info">
							<h4>{edu.degree} in {edu.field}</h4>
							<p class="institution">{edu.institution} • {edu.location}</p>
						</div>
						<div class="duration">
							<span class="duration-badge">{edu.duration}</span>
						</div>
					</div>
					
					{#if edu.gpa}
						<p class="gpa">GPA: {edu.gpa}</p>
					{/if}
					
					{#if edu.honors && edu.honors.length > 0}
						<div class="honors">
							<strong>Honors:</strong>
							{#each edu.honors as honor, index}
								<span class="honor">{honor}</span>{#if index < edu.honors.length - 1}, {/if}
							{/each}
						</div>
					{/if}
					
					{#if edu.relevantCourses && edu.relevantCourses.length > 0}
						<div class="courses">
							<strong>Relevant Coursework:</strong>
							<div class="course-tags">
								{#each edu.relevantCourses as course}
									<span class="course-tag">{course}</span>
								{/each}
							</div>
						</div>
					{/if}
				</div>
			{/each}
		</div>
	</div>
	
	<div class="certifications-section">
		<h3 class="subsection-title">Certifications</h3>
		<div class="certifications-grid">
			{#each certifications as cert}
				<div class="certification-card">
					<div class="cert-header">
						<h4>{cert.name}</h4>
						<span class="cert-date">{cert.date}</span>
					</div>
					<p class="cert-issuer">{cert.issuer}</p>
					
					<div class="cert-details">
						{#if cert.credentialId}
							<div class="cert-detail">
								<span class="detail-label">Credential ID:</span>
								<span class="detail-value">{cert.credentialId}</span>
							</div>
						{/if}
						{#if cert.validUntil}
							<div class="cert-detail">
								<span class="detail-label">Valid Until:</span>
								<span class="detail-value">{cert.validUntil}</span>
							</div>
						{/if}
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>

<style>
	.education-section, .certifications-section {
		margin-bottom: 2.5rem;
	}

	.certifications-section {
		margin-bottom: 0;
	}

	.subsection-title {
		font-size: 1.4rem;
		color: #e2e8f0;
		margin-bottom: 1.5rem;
		border-bottom: 1px solid #64748b;
		padding-bottom: 0.5rem;
	}

	.education-list {
		display: flex;
		flex-direction: column;
		gap: 2rem;
	}

	.education-item {
		position: relative;
		padding-left: 1.5rem;
		border-left: 3px solid #64748b;
	}

	.education-item::before {
		content: "";
		position: absolute;
		left: -6px;
		top: 0;
		width: 12px;
		height: 12px;
		background-color: #10b981;
		border-radius: 50%;
	}

	.education-header {
		display: flex;
		justify-content: space-between;
		align-items: flex-start;
		margin-bottom: 0.75rem;
		gap: 1rem;
	}

	.education-info h4 {
		font-size: 1.2rem;
		margin-bottom: 0.25rem;
	}

	.institution {
		color: #94a3b8 !important;
		font-weight: 500;
		margin-bottom: 0 !important;
	}

	.duration-badge {
		background-color: #059669;
		color: #dcfce7;
		padding: 0.25rem 0.75rem;
		border-radius: 1rem;
		font-size: 0.875rem;
		font-weight: 500;
		white-space: nowrap;
	}

	.gpa {
		color: #e2e8f0 !important;
		font-weight: 600;
		margin-bottom: 0.5rem !important;
	}

	.honors {
		margin-bottom: 1rem;
		color: #cbd5e1;
	}

	.honor {
		color: #059669;
		font-weight: 500;
	}

	.courses {
		color: #cbd5e1;
	}

	.course-tags {
		display: flex;
		flex-wrap: wrap;
		gap: 0.5rem;
		margin-top: 0.5rem;
	}

	.course-tag {
		background-color: #64748b;
		color: #f1f5f9;
		padding: 0.25rem 0.5rem;
		border-radius: 0.375rem;
		font-size: 0.875rem;
	}

	.certifications-grid {
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
		gap: 1.5rem;
	}

	.certification-card {
		background-color: #475569;
		border: 1px solid #64748b;
		border-radius: 0.75rem;
		padding: 1.5rem;
		transition: transform 0.2s ease;
	}

	.certification-card:hover {
		transform: translateY(-2px);
	}

	.cert-header {
		display: flex;
		justify-content: space-between;
		align-items: flex-start;
		margin-bottom: 0.5rem;
		gap: 1rem;
	}

	.cert-header h4 {
		margin-bottom: 0;
		font-size: 1.1rem;
	}

	.cert-date {
		background-color: #1e40af;
		color: #dbeafe;
		padding: 0.25rem 0.5rem;
		border-radius: 0.375rem;
		font-size: 0.875rem;
		font-weight: 500;
		white-space: nowrap;
	}

	.cert-issuer {
		color: #94a3b8 !important;
		font-weight: 500;
		margin-bottom: 1rem !important;
	}

	.cert-details {
		display: flex;
		flex-direction: column;
		gap: 0.5rem;
	}

	.cert-detail {
		display: flex;
		justify-content: space-between;
		font-size: 0.875rem;
	}

	.detail-label {
		color: #94a3b8;
	}

	.detail-value {
		color: #e2e8f0;
		font-weight: 500;
	}

	@media (max-width: 768px) {
		.education-header {
			flex-direction: column;
			gap: 0.5rem;
		}

		.duration-badge {
			align-self: flex-start;
		}

		.certifications-grid {
			grid-template-columns: 1fr;
		}

		.cert-header {
			flex-direction: column;
			gap: 0.5rem;
		}

		.cert-date {
			align-self: flex-start;
		}
	}
</style>
