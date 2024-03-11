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
	flex: 1; /* This will make sure that main takes all available space pushing footer to the bottom */
	padding: 3rem;
}

footer {
	width: 100%; /* Stretch footer across the width */
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
	padding: 6px;

	border-radius: 0; 
	position: relative; 
}

footer::before {
	content: '';
	position: absolute;
	top: 0;
	left: 0;
	height: 2px; 
	width: 100%;
}



@media (min-width: 480px) {
	footer {
		padding: 12px 0;
	}
}

</style>
