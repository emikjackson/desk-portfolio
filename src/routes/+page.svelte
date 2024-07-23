<script>
	import Desk from '$lib/components/Desk.svelte';
	import Section from '$lib/components/Section.svelte';
	import SectionImage from '$lib/components/SectionImage.svelte';
	import SectionContent from '$lib/components/SectionContent.svelte';
	import introImg from '$lib/assets/intro_cropped.png';
	import webImg from '$lib/assets/web.png';
	import artImg from '$lib/assets/art.png';
	import ProjectTiles from '$lib/components/ProjectTiles.svelte';
	import DevToolsList from '$lib/components/DevToolsList.svelte';
	import FooterLinks from '$lib/components/FooterLinks.svelte';
</script>

<Desk />

<Section divider={true}>
	<SectionImage
		src={introImg}
		alt="Waving smiling woman with dark, medium-length hair and crescent earrings"
		height="240px"
		width="268px"
	/>
	<SectionContent title="If you're new here ..." id="intro">
		<p>Let's get properly introduced!</p>
		<p>
			I'm a professional software engineer with a focus on <strong
				>full-stack web development</strong
			> and design. I find satisfaction in building high quality, accessible web applications.
		</p>
		<p>
			I also love learning and helping others learn new scientific concepts. I recently worked as a
			museum
			<strong>science educator</strong>, and these days you can often find me reading about ecology
			and relativity in physics.
		</p>
		<p>
			On the more creative side of things, I enjoy drawing, painting, occasional music-making, and
			sewing/mending.
		</p>
		<p>
			If you're here, you may be interested in working with me. If so, reach out anytime at <a
				href="mailto:emikjackson@gmail.com?subject=Website Contact"
			>
				emikjackson@gmail.com</a
			>.
		</p>
	</SectionContent>
</Section>

<Section secondary={true} flip={true} style="margin-bottom: 20px;">
	<SectionContent title="Web development" id="web">
		<p>
			Here are some common pieces in my development process, along with my most frequently used
			applications, languages, and libraries.
		</p>
		<DevToolsList />
		<p>
			Check out my <a
				href="https://github.com/emikjackson"
				rel="noopener noreferrer"
				target="_blank">GitHub profile</a
			> or see below for recent project examples.
		</p>
	</SectionContent>
	<SectionImage
		src={webImg}
		alt="web page broken down as if being designed and interacted with, with a leaf visual and map"
		width="390px"
		height="248px"
	/>
</Section>

<Section secondary={true} nested={true}>
	<SectionContent title="Recent projects" subtitle={true} id="web">
		<p>
			While much of my professional work has been done collaboratively on teams, here are a couple
			of recent projects I've created individually to try out new concepts.
		</p>
		<ProjectTiles />
	</SectionContent>
</Section>

<Section flip={true}>
	<SectionContent title="Art & Animation" id="art">
		<p>Not professionally, I also like to draw, paint, sew, etc!</p>
		<p>Will add a small portfolio or link here soon.</p>
	</SectionContent>
	<SectionImage
		src={artImg}
		alt="Paper with stick figure animation frames next to cup with pens, pencils, and paintbrush"
		height="260px"
		width="329px"
	/>
</Section>

<FooterLinks />
