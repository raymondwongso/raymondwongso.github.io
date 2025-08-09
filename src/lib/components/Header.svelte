<script lang="ts">
	// Personal information
	const personalInfo = {
		name: "Raymond Wongso",
		title: "Lead Backend Engineer at Stockbit",
		location: "Surabaya, Indonesia",
		email: "raymondwongso.work@gmail.com",
		linkedin: "www.linkedin.com/in/-raymondwongsohartanto/",
		github: "github.com/raymondwongso",
		website: "raymondwongso.github.io"
	};
</script>

<header class="section">
	<div class="header-content">
		<div class="personal-info">
			<h1>{personalInfo.name}</h1>
			<p class="title">{personalInfo.title}</p>
			<p class="location">{personalInfo.location}</p>
		</div>
		
		<div class="contact-info">
			<div class="contact-item">
				<svg class="icon" viewBox="0 0 24 24" fill="currentColor">
					<path d="M24 5.457v13.909c0 .904-.732 1.636-1.636 1.636h-3.819V11.73L12 16.64l-6.545-4.91v9.273H1.636A1.636 1.636 0 0 1 0 19.366V5.457c0-.887.732-1.636 1.636-1.636h.887l9.477 7.055 9.477-7.055h.887c.904 0 1.636.749 1.636 1.636z"/>
				</svg>
				<a href="mailto:{personalInfo.email}">{personalInfo.email}</a>
			</div>
			<div class="contact-item">
				<svg class="icon" viewBox="0 0 24 24" fill="currentColor">
					<path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
				</svg>
				<a href="https://{personalInfo.linkedin}" target="_blank" rel="noopener">LinkedIn</a>
			</div>
			<div class="contact-item">
				<svg class="icon" viewBox="0 0 24 24" fill="currentColor">
					<path d="M12 0C5.374 0 0 5.373 0 12 0 17.302 3.438 21.8 8.207 23.387c.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23A11.509 11.509 0 0 1 12 5.803c1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576C20.566 21.797 24 17.3 24 12c0-6.627-5.373-12-12-12z"/>
				</svg>
				<a href="https://{personalInfo.github}" target="_blank" rel="noopener">GitHub</a>
			</div>
			<div class="contact-item">
				<svg class="icon" viewBox="0 0 24 24" fill="currentColor">
					<path d="M12 0C5.374 0 0 5.373 0 12s5.374 12 12 12 12-5.373 12-12S18.626 0 12 0zm5.568 8.16c-.169 1.858-.896 3.593-2.043 4.741-1.146 1.147-2.881 1.874-4.739 2.043-.362.03-.728.045-1.095.045s-.733-.015-1.095-.045c-1.858-.169-3.593-.896-4.739-2.043C2.71 11.753 1.983 10.018 1.814 8.16 1.784 7.798 1.769 7.432 1.769 7.065s.015-.733.045-1.095c.169-1.858.896-3.593 2.043-4.739C5.004.084 6.739-.643 8.597-.812 8.959-.842 9.325-.857 9.692-.857s.733.015 1.095.045c1.858.169 3.593.896 4.739 2.043 1.147 1.146 1.874 2.881 2.043 4.739.03.362.045.728.045 1.095s-.015.733-.045 1.095zm-1.095 0c-.169-1.858-.896-3.593-2.043-4.739C13.284 2.274 11.549 1.547 9.691 1.378 9.329 1.348 8.963 1.333 8.596 1.333s-.733.015-1.095.045C5.643 1.547 3.908 2.274 2.761 3.421 1.614 4.567.887 6.302.718 8.16.688 8.522.673 8.888.673 9.255s.015.733.045 1.095c.169 1.858.896 3.593 2.043 4.739 1.147 1.147 2.882 1.874 4.74 2.043.362.03.728.045 1.095.045s.733-.015 1.095-.045c1.858-.169 3.593-.896 4.739-2.043 1.147-1.146 1.874-2.881 2.043-4.739.03-.362.045-.728.045-1.095s-.015-.733-.045-1.095z"/>
				</svg>
				<a href="https://{personalInfo.website}" target="_blank" rel="noopener">Website</a>
			</div>
		</div>
	</div>
</header>

<style>
	.section {
		margin-bottom: 1.5rem;
	}

	.header-content {
		display: flex;
		flex-direction: column;
		gap: 1rem;
	}

	.personal-info h1 {
		margin: 0 0 0.5rem 0;
		color: #f1f5f9;
		font-size: 2.125rem;
		font-weight: 700;
	}

	.title {
		margin: 0 0 0.25rem 0;
		color: #94a3b8;
		font-size: 1.075rem;
		font-weight: 500;
	}

	.location {
		margin: 0;
		color: #64748b;
		font-size: 0.825rem;
	}

	.contact-info {
		display: flex;
		flex-direction: column;
		gap: 0.5rem;
	}

	.contact-item {
		display: flex;
		align-items: center;
		gap: 0.5rem;
	}

	.icon {
		width: 18px;
		height: 18px;
		color: #3b82f6;
		flex-shrink: 0;
	}

	.contact-item a {
		color: #cbd5e1;
		text-decoration: none;
		font-size: 0.825rem;
		word-break: break-all;
	}

	.contact-item a:hover {
		color: #3b82f6;
		text-decoration: underline;
	}

	@media (max-width: 1024px) {
		.contact-info {
			flex-direction: row;
			flex-wrap: wrap;
			gap: 1rem;
		}

		.contact-item {
			flex: 1;
			min-width: 120px;
		}
	}
</style>
