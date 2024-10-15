<script>
	import DimensionalLink from './DimensionalLink.svelte';
	import footer from '$lib/assets/games/footer.svg';
	import AnimatedHeart from './AnimatedHeart.svelte';
</script>

<div class="wrapper">
	<div class="content">
		<div class="hero">
			<h1 class="lalezar title">Games</h1>
			<AnimatedHeart />
		</div>
		<p>
			Hi! Welcome to my unlinked games section. Although I've spent most of my professional career
			as a web developer, I'm drawn to the process of making games and other immersive experiences.
			I would love to create full-fledged, story driven games that expand a player's worldview.
		</p>

		<h3>Game and Asset Creation Toolkit</h3>
		<ul>
			<li>Godot</li>
			<li>Unity</li>
			<li>Bitsy</li>
			<li>HTML/CSS/JS</li>
			<li class="design">Sketch/Figma</li>
			<li class="design">Procreate</li>
			<li class="design">Photoshop</li>
			<li class="design">Physical Art</li>
		</ul>

		<h2 class="lalezar break">Sew Sew</h2>
		<p class="subheader">Godot, Physical Art, 2024</p>
		<p>
			My current project! Planning on it being a mostly point and click game utilizing photographs
			of a real-world miniature set as the primary visuals.
		</p>
		<p>
			Help out Z at her sewing and mending shop for a few weeks. Dive into the world of modern
			textiles, and perhaps find yourself discovering more about the fabric of space and time?
		</p>

		<h2 class="lalezar break">A May Morning</h2>
		<p class="subheader">Bitsy, Pixel Art, 2024</p>
		<p>An itsy bitsy game, created for a Bitsy jam.</p>
		<p>
			Walk through a spring morning out in the garden, led by your cat. This quick narrative game is
			inspired by my daily morning routine and memories of gardening with my grandma May.
		</p>
		<DimensionalLink link="https://movingaround.itch.io/a-may-morning"
			>Play it on Itch</DimensionalLink
		>

		<h2 class="lalezar break">Ear Trainer 3000</h2>
		<p class="subheader">HTML/CSS/JS, 2024</p>
		<p>A little listen-and-guess music quiz, made at the request of my father.</p>
		<p>
			How well can you identify a sequence of notes, given the key? Click around and train your ear,
			with a few difficulty settings available. Style inspired by an electronic metronome I
			practiced with growing up.
		</p>
		<DimensionalLink link="https://ear-trainer-3000.vercel.app/"
			>Play the guessing-game</DimensionalLink
		>

		<h2 class="lalezar break">It's a Colorful World</h2>
		<p class="subheader">Unity, Sketch, 2019</p>
		<p>
			Two-week solo project created for a game development course at the University of Michigan.
		</p>
		<p>
			It's a Colorful World is an adventure game in which the player uses a simple walking /
			speed-walking mechanic to steal color crystals from BleakBroadcasting and restore color to
			this grey-scale world. Talk to residents, avoid guards and energized color balls, then nab the
			primary color crystals - just watch out for the (not so difficult) Evil Boss Man!
		</p>
		<DimensionalLink link="https://movingaround.itch.io/its-a-colorful-world">
			Download Mac app on Itch
		</DimensionalLink>

		<h2 class="lalezar break">Off the Deep End</h2>
		<p class="subheader">Unity, Sketch, 2019</p>
		<p>
			Cooperative team project created for a game development course at the University of Michigan.
			I created all of the assets in Sketch and programmed character + enemy movement and
			interactions, all animations, and final crab boss battle in Unity.
		</p>
		<p>
			When a deep-ocean explorer is suddenly taken by a giant crab, their 4 friends must
			cooperatively venture into the depths of the sea on a rescue mission. Their high tech
			submarine allows them to bust through rock and fend off dangerous fish, but remains vulnerable
			to running out of air.
		</p>
		<DimensionalLink link="https://www.indiedb.com/games/off-the-deep-end">
			View the Indie DB logs
		</DimensionalLink>
		<div class="footer">
			<img width={120} height={80} src={footer} alt="a red heart and a magnifying glass" />
		</div>
	</div>
</div>

<style>
	.hero {
		display: flex;
		align-items: center;
		gap: 30px;
	}
	.title {
		font-size: 5rem;
	}
	h2.break {
		font-size: 3rem;
		padding-top: 10px;
		margin-top: 30px;
		margin-bottom: 0px;
		border-top: 1px solid rgba(0, 0, 0, 0.1);
	}
	p.subheader {
		margin-top: 0px;
		font-style: italic;
	}
	.wrapper {
		display: flex;
		flex-direction: column;
		align-items: center;
	}
	.content {
		width: 1000px;
		max-width: 100%;
		box-sizing: border-box;
		padding: 40px 20px;
	}
	ul {
		list-style-type: none;
		margin: 0px;
		padding: 0px;
		display: flex;
		flex-wrap: wrap;
		justify-content: flex-start;
		align-items: center;
		gap: 10px;
	}
	li {
		padding: 8px 18px;
		border-radius: 18px;
		background-color: #592377;
		color: #f6f2f5;
	}
	li.design {
		background-color: #92318a;
	}
	.footer {
		display: flex;
		justify-content: center;
		align-items: center;
		margin-top: 20px;
		padding: 20px;
	}
</style>
