<!-- Simplified header for games page -->

<nav aria-labelledby="nav-label">
	<h2 id="nav-label" class="visually-hidden">Main Menu</h2>
	<ul>
		<li><a href="/" class="title">EJ</a></li>
		<li><a href="/">← Go to EJ home</a></li>
	</ul>
</nav>

<style>
	.title {
		color: var(--text-color);
		text-decoration: none;
		font-weight: 800;
		font-size: 2rem;
		text-shadow: 2px 2px 0px #9bc3ff;
		transition: text-shadow 0.2s linear;
	}
	.title:hover {
		text-shadow: 3px 3px 0px #b7e3ff;
	}
	a {
		font-weight: 600;
	}
	ul {
		list-style-type: none;
		margin: 0px;
		padding: 0px;
		display: flex;
		justify-content: flex-end;
		align-items: center;
		padding: 8px 16px;
		gap: 10px;
	}
	li:first-child {
		margin-right: auto;
	}
	li {
		margin: 0px;
	}
</style>
