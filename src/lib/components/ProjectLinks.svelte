<script>
	/**
	 * GitHub and project icon links! Includes visually-hidden text for screenreaders.
	 */
	import GithubIcon from './icons/GithubIcon.svelte';

	export let githubLink = ''; // optional
</script>

{#if githubLink}
	<a href={githubLink} rel="noopener noreferrer" target="_blank">
		<div class="visually-hidden">View GitHub</div>
		<GithubIcon />
	</a>
{/if}

<style>
	a {
		color: var(--text-color);
		text-decoration: none;
		display: inline-flex;
		align-items: center;
		height: 1.5rem;
		font-weight: 600;
		transition: background-color 0.2s ease;
	}
	a:hover {
		color: #000;
	}
</style>
