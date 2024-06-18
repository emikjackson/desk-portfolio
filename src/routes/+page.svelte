<script>
	import Desk from '$lib/components/Desk.svelte';
	import Section from '$lib/components/Section.svelte';
	import SectionImage from '$lib/components/SectionImage.svelte';
	import SectionContent from '$lib/components/SectionContent.svelte';
	import introImg from '$lib/assets/intro.png';
	import ProjectCards from '$lib/components/ProjectCards.svelte';
	import ReferenceLinks from '$lib/components/ReferenceLinks.svelte';
</script>

<Desk />

<Section>
	<SectionImage
		src={introImg}
		alt="Waving smiling woman with dark hair and crescent earrings"
		height="260px"
	/>
	<SectionContent title="If you're new here ..." id="intro">
		<p>Let's get properly introduced!</p>
		<p>
			I'm a professional software engineer with a focus on full-stack web development and design. I
			especially love building high quality, accessible tools that <strong
				>promote social equity</strong
			>
			and
			<strong>explore science concepts</strong>.
		</p>
		<p>
			I also make silly websites for family & friends, and enjoy working with others on creative
			projects (drawing, animation, sewing).
		</p>
		<p>
			If you're visiting this site, you may be interesting in hiring or working on something
			creative with me.
		</p>
		<p>
			If so, contact me anytime at <a href="mailto:emikjackson@gmail.com?subject=Website Contact">
				emikjackson@gmail.com
			</a>.
		</p>
	</SectionContent>
</Section>

<Section secondary={true} divider={false}>
	<SectionContent title="Web development" id="web">
		<p>
			What does it mean to build websites or web tools? Here's what typically goes into one of my
			web development projects.
		</p>
		<ul>
			<li>Dynamic user interface</li>
			<li>Data procurement assitance / web scraping</li>
			<li>User experience testing</li>
		</ul>
		<p>I've helped create many professional websites, both individually and on teams.</p>
		<p>
			Outside of building professional websites, I also like making some sites for personal
			enjoyment or for loved ones.
		</p>
		<p>For more details and recent examples, check out my resume or GitHub profile.</p>
		<ReferenceLinks />
	</SectionContent>
	<SectionImage
		src={introImg}
		alt="Waving smiling woman with dark hair and crescent earrings"
		height="260px"
	/>
</Section>
