<script>
	import clientNoteTrackerImg from '$lib/assets/projects/client_note_tracker.png';
	import earTrainerImg from '$lib/assets/projects/ear_trainer.png';
	import fertilizerMapImg from '$lib/assets/projects/fertilizer_map.png';
	import awcsImg from '$lib/assets/projects/awcs.png';
	import ProjectLinks from './ProjectLinks.svelte';

	const projects = [
		{
			title: 'Client Note Tracker',
			text: 'Developed complete frontend and backend routes for a simple note taking application.',
			technologies: ['Svelte', 'Django', 'PostgreSQL'],
			image: clientNoteTrackerImg,
			siteLink: 'https://www.clientnotetracker.com/'
		},
		{
			title: '8 Dynamics of Climate Engagement Quiz',
			text: 'Collaborated on a quiz application for the All We Can Save project, allowing users to gauge their climate engagement and access resources.',
			technologies: ['Svelte', 'Mailchimp Transactional API'],
			image: awcsImg,
			siteLink: 'https://dynamics-quiz.allwecansave.earth/'
		},
		{
			title: 'Ear Trainer 3000',
			text: 'A little listen-and-guess music quiz, for funsies. Style inspired by an electronic metronome I practiced with growing up.',
			technologies: ['Svelte', 'AudioContext'],
			image: earTrainerImg,
			siteLink: 'https://ear-trainer-3000.vercel.app/',
			githubLink: 'https://github.com/emikjackson/ear-trainer-3000'
		},
		{
			title: 'Fertilizer Usage in the U.S.',
			text: 'Exploring estimated Nitrogen & Phosphorus fertilizer usage by county from 1950-2017. Data from USGS.',
			technologies: ['React', 'Leaflet', 'Python'],
			image: fertilizerMapImg,
			siteLink: 'https://fertilizer-map.vercel.app/',
			githubLink: 'https://github.com/emikjackson/fertilizer-map'
		}
		// {
		// 	title: 'We Like Soup',
		// 	text: "Made this small soup site to explore SVG animations, while highlighting some of my coworkers' favorite soups.",
		// 	technologies: ['Svelte', 'SVG animation with JS+CSS'],
		// 	image: soupImg,
		// 	siteLink: 'https://we-like-soup.vercel.app/',
		// 	githubLink: 'https://github.com/emikjackson/we-like-soup'
		// }
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
				<ProjectLinks githubLink={project.githubLink} />
			</div>
			<p>
				{project.text}

				{#if project.githubLink}
					<a href={project.githubLink} rel="noopener noreferrer" target="_blank">View code</a>
				{/if}
			</p>
			<div class="technologies">
				{project.technologies.join(', ')}
			</div>
		</div>
	{/each}
</div>

<style>
	.wrapper {
		margin-top: 26px;
		display: flex;
		flex-wrap: wrap;
		gap: 26px 2%;
	}
	.tile {
		width: 49%;
		box-sizing: border-box;
	}
	.tile img {
		width: 100%;
		height: 240px;
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
	p a {
		font-style: italic;
	}
	@media (max-width: 1000px) {
		.wrapper {
			gap: 30px;
		}
		.tile {
			flex: auto;
			margin-top: 10px;
		}
	}
</style>
