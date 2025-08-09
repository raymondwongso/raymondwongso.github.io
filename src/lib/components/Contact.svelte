<script lang="ts">
	// Sample contact information - replace with your actual details
	const contactInfo = {
		email: "raymondwongso.work@gmail.com",
		phone: "+1 (555) 123-4567",
		linkedin: "www.linkedin.com/in/-raymondwongsohartanto",
		github: "github.com/raymondwongso",
		location: "Surabaya, Indonesia",
		website: "raymondwongso.github.io"
	};

	const socialLinks = [
		{
			name: "LinkedIn",
			url: `https://${contactInfo.linkedin}`,
			icon: "💼"
		},
		{
			name: "GitHub",
			url: `https://${contactInfo.github}`,
			icon: "💻"
		},
		{
			name: "Website",
			url: `https://${contactInfo.website}`,
			icon: "🌐"
		}
	];
</script>

<section class="section">
	<h2>Get In Touch</h2>
	
	<div class="contact-content">
		<div class="contact-text">
			<p class="contact-intro">
				I'm always interested in new opportunities and exciting projects. 
				Whether you're looking to hire, collaborate, or just want to connect, 
				feel free to reach out!
			</p>
			
			<div class="contact-methods">
				<div class="contact-method">
					<span class="method-icon">📧</span>
					<div class="method-info">
						<span class="method-label">Email</span>
						<a href="mailto:{contactInfo.email}" class="method-value">{contactInfo.email}</a>
					</div>
				</div>
				
				<div class="contact-method">
					<span class="method-icon">📱</span>
					<div class="method-info">
						<span class="method-label">Phone</span>
						<a href="tel:{contactInfo.phone.replace(/\s+/g, '')}" class="method-value">{contactInfo.phone}</a>
					</div>
				</div>
				
				<div class="contact-method">
					<span class="method-icon">📍</span>
					<div class="method-info">
						<span class="method-label">Location</span>
						<span class="method-value">{contactInfo.location}</span>
					</div>
				</div>
			</div>
		</div>
		
		<div class="social-links">
			<h3>Connect With Me</h3>
			<div class="social-grid">
				{#each socialLinks as social}
					<a 
						href={social.url} 
						target="_blank" 
						rel="noopener noreferrer"
						class="social-link"
					>
						<span class="social-icon">{social.icon}</span>
						<span class="social-name">{social.name}</span>
					</a>
				{/each}
			</div>
		</div>
	</div>
	
	<div class="contact-footer">
		<p>Thank you for taking the time to review my profile. I look forward to hearing from you!</p>
	</div>
</section>

<style>
	.contact-content {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: 3rem;
		margin-bottom: 2rem;
	}

	.contact-intro {
		font-size: 1.1rem;
		line-height: 1.7;
		margin-bottom: 2rem;
		color: #4b5563;
	}

	.contact-methods {
		display: flex;
		flex-direction: column;
		gap: 1.5rem;
	}

	.contact-method {
		display: flex;
		align-items: center;
		gap: 1rem;
	}

	.method-icon {
		font-size: 1.5rem;
		width: 40px;
		text-align: center;
	}

	.method-info {
		display: flex;
		flex-direction: column;
		gap: 0.25rem;
	}

	.method-label {
		font-size: 0.875rem;
		font-weight: 600;
		color: #6b7280;
		text-transform: uppercase;
		letter-spacing: 0.05em;
	}

	.method-value {
		font-size: 1rem;
		color: #374151;
		font-weight: 500;
	}

	.method-value:where(a) {
		color: #2563eb;
		text-decoration: none;
		transition: color 0.2s ease;
	}

	.method-value:where(a):hover {
		color: #1d4ed8;
		text-decoration: underline;
	}

	.social-links h3 {
		margin-bottom: 1.5rem;
		color: #374151;
	}

	.social-grid {
		display: flex;
		flex-direction: column;
		gap: 1rem;
	}

	.social-link {
		display: flex;
		align-items: center;
		gap: 1rem;
		padding: 1rem;
		background-color: #f9fafb;
		border: 1px solid #e5e7eb;
		border-radius: 0.75rem;
		text-decoration: none;
		color: #374151;
		transition: all 0.2s ease;
	}

	.social-link:hover {
		background-color: #2563eb;
		color: white;
		transform: translateY(-2px);
		box-shadow: 0 4px 12px rgba(37, 99, 235, 0.2);
	}

	.social-icon {
		font-size: 1.5rem;
		width: 32px;
		text-align: center;
	}

	.social-name {
		font-weight: 500;
	}

	.contact-footer {
		text-align: center;
		padding: 2rem 0;
		border-top: 1px solid #e5e7eb;
		margin-top: 2rem;
	}

	.contact-footer p {
		font-style: italic;
		color: #6b7280;
		margin-bottom: 0;
	}

	@media (max-width: 768px) {
		.contact-content {
			grid-template-columns: 1fr;
			gap: 2rem;
		}

		.contact-methods {
			gap: 1rem;
		}

		.contact-method {
			flex-direction: column;
			align-items: flex-start;
			gap: 0.5rem;
		}

		.method-icon {
			width: auto;
		}

		.social-grid {
			gap: 0.75rem;
		}

		.social-link {
			padding: 0.75rem;
		}
	}
</style>
