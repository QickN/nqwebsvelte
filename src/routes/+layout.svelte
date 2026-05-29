<script>
	import Header from './Header.svelte';
	import './styles.css';

	const year = new Date().getFullYear();
</script>

<div class="site-shell">
	<Header />

	<main class="page-frame">
		<slot />
	</main>

	<footer class="site-footer">
		<span>&copy; {year} Nick Quam. Built with care in Colorado.</span>
		<div class="footer-links" aria-label="External links">
			<a href="https://astretto.com" target="_blank" rel="noreferrer">Astretto</a>
			<a href="https://checkoutrankings.com" target="_blank" rel="noreferrer">Checkout</a>
			<a href="https://github.com/QickN" target="_blank" rel="noreferrer">GitHub</a>
		</div>
	</footer>
</div>
