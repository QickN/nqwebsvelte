<script>
	import { page } from '$app/stores';

	const links = [
		{ href: '/', label: 'Home' },
		{ href: '/projects', label: 'Work' },
		{ href: '/skills', label: 'Profile' }
	];
</script>

<header class="top-nav" aria-label="Primary navigation">
	<a href="/" class="brand" aria-label="Nick Quam home">
		<span class="mark">N</span>
		<span class="brand-text">
			<strong>Nick Quam</strong>
			<span>Engineers solutions</span>
		</span>
	</a>

	<nav class="nav-links" aria-label="Site">
		{#each links as link}
			<a href={link.href} class:active={$page.url.pathname === link.href}>{link.label}</a>
		{/each}
	</nav>
</header>
