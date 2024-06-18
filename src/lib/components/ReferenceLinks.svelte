<script>
	/**
	 * GitHub and resume reference styled links!
	 */
	import githubCatIcon from '$lib/assets/github_cat.png';
</script>

<div>
	<a href="https://github.com/emikjackson" rel="noopener noreferrer" target="_blank">
		View GitHub
		<!-- Skipping alt tag since link is already described -->
		<img class="github" src={githubCatIcon} alt="" />
	</a>

	<a
		href="https://drive.google.com/file/d/11yiWgSXQfSuyOpJDjODFkL6Af0oCmIB_/view?usp=sharing"
		rel="noopener noreferrer"
		target="_blank"
		class="secondary"
	>
		View Resume
	</a>
</div>

<style>
	a {
		padding: 8px 12px;
		border-radius: 2px;
		background-color: #077083;
		box-shadow: 0px 2px 4px 0px rgba(0, 0, 0, 0.1);
		color: white;
		margin-right: 5px;
		text-decoration: none;
		border: 1px solid #077083;
		display: inline-flex;
		align-items: center;
		height: 1.5rem;
		font-weight: 600;
		transition: background-color 0.2s ease;
	}
	a:hover,
	a:focus {
		background-color: #056576;
	}
	a.secondary {
		color: #077083;
		background-color: white;
	}
	a.secondary:hover,
	a.secondary:focus {
		background-color: #f2f6fa;
	}
	img.github {
		width: 1.45rem;
		height: 1.45rem;
		margin-left: 8px;
	}
</style>
