<script>
	import Header from './Header.svelte';
	import './styles.css';
</script>

<div class="app">
	<Header />

	<main>
		<slot />
	</main>

	<footer class="glass-effect">
		<p>created by <strong>nick</strong></p>
	</footer>
</div>

<style>
.app {
	display: flex;
	flex-direction: column;
	min-height: 100vh;
}

main {
	flex: 1;
	padding: 2rem 1rem;
	max-width: 1200px;
	width: 100%;
	margin: 0 auto;
}

footer {
	width: 100%;
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
	padding: 1.5rem;
	margin-top: 2rem;
	background-color: rgba(0, 0, 0, 0.2);
	backdrop-filter: blur(10px);
	border-top: 1px solid rgba(255, 255, 255, 0.1);
	box-shadow: 0 -10px 30px rgba(0, 0, 0, 0.1);
	position: relative;
}

footer p {
	margin: 0;
	font-size: 0.9rem;
	letter-spacing: 0.03em;
}

footer p strong {
	color: var(--color-theme-1);
	font-weight: 600;
}

@media (min-width: 768px) {
	main {
		padding: 3rem 2rem;
	}

	footer {
		padding: 1.75rem;
	}
}

</style>
