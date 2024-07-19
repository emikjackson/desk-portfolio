<script>
	import clientNoteTrackerImg from '$lib/assets/projects/client_note_tracker.png';
	import earTrainerImg from '$lib/assets/projects/ear_trainer.png';
	import fertilizerMapImg from '$lib/assets/projects/fertilizer_map.png';
	import ProjectLinks from './ProjectLinks.svelte';
	import GithubLink from './ProjectLinks.svelte';

	const projects = [
		{
			title: 'Client Note Tracker',
			text: 'Web version for note taking application.',
			technologies: ['Svelte', 'Django', 'PostgreSQL'],
			image: clientNoteTrackerImg,
			siteLink: 'https://www.clientnotetracker.com/'
		},
		{
			title: 'Ear Trainer 3000',
			text: 'Listen-and-guess music quiz, for funsies.',
			technologies: ['Svelte', 'AudioContext'],
			image: earTrainerImg,
			siteLink: 'https://ear-trainer-3000.vercel.app/',
			githubLink: 'https://github.com/emikjackson/ear-trainer-3000'
		},
		{
			title: 'Fertilizer Usage in the USA',
			text: 'Exploring Nitrogen & Phosphorus fertilizer usage by county from 1950-2017.',
			technologies: ['React', 'Leaflet', 'Python'],
			image: fertilizerMapImg,
			siteLink: '',
			githubLink: 'https://github.com/emikjackson/fertilizer-map'
		}
	];
</script>

<div class="wrapper">
	{#each projects as project}
		<div class="tile">
			<a href={project.siteLink} rel="noopener noreferrer" target="_blank">
				<img src={project.image} alt="" />
			</a>
			<div class="header">
				<a href={project.siteLink} rel="noopener noreferrer" target="_blank">
					<h3>{project.title}</h3>
				</a>
				<ProjectLinks githubLink={project.githubLink} siteLink={project.siteLink} />
			</div>
			<p>{project.text}</p>
			<div class="technologies">
				{project.technologies.join(', ')}
				<!-- {#each project.technologies as technologyItem}
					<div class="technology-item">{technologyItem}</div>
				{/each} -->
			</div>
		</div>
	{/each}
</div>

<style>
	.wrapper {
		display: flex;
		gap: 15px;
	}
	.tile {
		flex: 1;
	}
	.tile img {
		width: 100%;
		height: 180px;
		object-fit: cover;
		border: 1px solid rgb(229, 229, 229);
		border-radius: 4px;
	}
	h3 {
		margin: 0px;
		margin-right: 4px;
	}
	a {
		color: var(--text-color);
	}
	.header {
		display: flex;
		justify-content: flex-start;
		align-items: center;
		gap: 5px;
		margin-top: 10px;
	}
	.technologies {
		color: grey;
		font-style: italic;
	}
	@media (max-width: 1000px) {
		.wrapper {
			flex-wrap: wrap;
			gap: 40px;
		}
		.tile {
			flex: auto;
			margin-top: 10px;
		}
	}
</style>
