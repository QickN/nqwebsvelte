<script>
	import { page } from '$app/stores';
	import logo from '$lib/images/svelte-logo.svg';
	import github from '$lib/images/github.svg';
</script>

<header class="glass-nav">
	<div class="corner">
		<a href="/" class="logo-link">NQ</a>
	</div>

	<nav>
		<ul>
			<li aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
				<a href="/">Home</a>
			</li>
			<li aria-current={$page.url.pathname === '/projects' ? 'page' : undefined}>
				<a href="/projects">Projects</a>
			</li>
			<li aria-current={$page.url.pathname === '/skills' ? 'page' : undefined}>
				<a href="/skills">Skills</a>
			</li>
		</ul>
	</nav>

	<div class="corner social">
		<a href="https://github.com/qickn" target="_blank" class="social-link">
			<img src={github} alt="GitHub" />
		</a>
	</div>
</header>

<style>
	header {
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding: 1rem 2rem;
		margin: 1rem 2rem;
		border-radius: 16px;
	}

	.glass-nav {
		background: rgba(0, 0, 0, 0.2);
		backdrop-filter: blur(10px);
		box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
		border: 1px solid rgba(255, 255, 255, 0.1);
	}

	.corner {
		width: 3em;
		height: 3em;
		display: flex;
		align-items: center;
	}

	.logo-link {
		font-family: var(--font-heading);
		font-weight: 700;
		font-size: 1.5rem;
		color: white;
		text-decoration: none;
		letter-spacing: -0.05em;
	}

	.logo-link:hover {
		color: var(--color-theme-1);
	}

	.corner a {
		display: flex;
		align-items: center;
		justify-content: center;
		transition: transform 0.3s ease;
	}

	.corner a:hover {
		transform: scale(1.1);
	}

	.corner.social {
		justify-content: flex-end;
	}

	.corner img {
		width: 1.75em;
		height: 1.75em;
		object-fit: contain;
		filter: invert(1); /* Makes GitHub icon white */
	}

	nav {
		display: flex;
		justify-content: center;
	}

	ul {
		position: relative;
		padding: 0;
		margin: 0;
		height: 3em;
		display: flex;
		justify-content: center;
		align-items: center;
		list-style: none;
		gap: 1.5rem;
	}

	li {
		position: relative;
		height: 100%;
	}

	li[aria-current='page'] a {
		color: white;
		position: relative;
	}

	li[aria-current='page'] a::after {
		content: '';
		position: absolute;
		bottom: -4px;
		left: 0;
		width: 100%;
		height: 2px;
		background-color: var(--color-theme-1);
		border-radius: 2px;
	}

	nav a {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 0.5rem;
		color: rgba(255, 255, 255, 0.8);
		font-weight: 500;
		font-size: 0.95rem;
		text-decoration: none;
		transition: all 0.3s ease;
	}

	a:hover {
		color: white;
	}

	@media (max-width: 768px) {
		header {
			padding: 0.75rem 1rem;
			margin: 0.5rem 1rem;
		}

		ul {
			gap: 0.75rem;
		}

		nav a {
			font-size: 0.85rem;
			padding: 0 0.3rem;
		}
	}
</style>
