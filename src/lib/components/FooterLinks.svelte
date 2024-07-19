<script>
	import EmailIcon from './icons/EmailIcon.svelte';
	import GithubIcon from './icons/GithubIcon.svelte';
	import LinkedInIcon from './icons/LinkedInIcon.svelte';
</script>

<div class="footer">
	<a href="mailto:emikjackson@gmail.com" style="margin-right:2px;">
		<div class="visually-hidden">Email me</div>
		<EmailIcon width={36} />
	</a>
	<a href="https://github.com/emikjackson" rel="noopener noreferrer">
		<div class="visually-hidden">Github</div>
		<GithubIcon width={36} />
	</a>
	<a href="https://www.linkedin.com/in/emi-jackson-a313b7139/" rel="noopener noreferrer">
		<div class="visually-hidden">LinkedIn</div>
		<LinkedInIcon width={36} />
	</a>
</div>

<style>
	.footer {
		display: flex;
		justify-content: center;
		align-items: center;
		gap: 20px;
		margin: 80px 20px;
		margin-bottom: 40px;
	}
	a {
		color: var(--text-color);
	}
</style>
