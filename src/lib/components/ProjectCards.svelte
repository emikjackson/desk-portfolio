<script>
	import LinkButton from './LinkButton.svelte';

	const projects = [
		{
			title: 'Note Sequence Guesser',
			text: 'A music game to help my dad train his ear',
			technologies: ['Svelte', 'SvelteKit', 'Synth?', 'Vercel'],
			siteLink: 'https://music-notes.vercel.app/',
			githubLink: 'https://github.com/emikjackson/music-notes'
		}
	];
</script>

<div class="wrapper">
	{#each projects as project}
		<div class="card">
			<h3>{project.title}</h3>
			<p>{project.text}</p>
			<div class="technologies">
				{#each project.technologies as technologyItem}
					<div class="technology-item">{technologyItem}</div>
				{/each}
			</div>
			<LinkButton href={project.siteLink}>View site</LinkButton>
			<LinkButton href={project.githubLink} secondary>GitHub</LinkButton>
		</div>
	{/each}
</div>

<style>
	.wrapper {
		display: flex;
		margin-left: -5px;
	}
	.card {
		background-color: #fff;
		padding: 5px 10px;
		border-radius: 4px;
		border: 1px solid #f0f0f0;
	}
	h3 {
		margin: 0px;
	}
	.technologies {
		display: flex;
	}
	.technology-item {
		border: 1px solid #f0f0f0;
		padding: 2px 4px;
		border-radius: 4px;
		margin-right: 4px;
	}
</style>
