<script>
	import { goto } from "$app/navigation";
	import { onMount } from "svelte";

	let visible = false;

	onMount(() => {
		// Add a small delay before showing content for smooth animation
		setTimeout(() => {
			visible = true;
		}, 300);
	});
</script>

<svelte:head>
    <title>Nick Quam | Portfolio</title>
    <meta name="description" content="Nick Quam's Portfolio - Software Engineer and Developer" />
</svelte:head>

<main>
    <section class="hero" class:visible>
        <div class="content-container">
            <div class="text-content">
                <h1>Nick Quam</h1>
                <p class="tagline">Software Engineer & Developer</p>
                <p class="description">
                    Creating elegant solutions through code and design.
                </p>
                <div class="button-container">
                    <button class="primary-btn" on:click={() => goto('/projects')}>View Projects</button>
                    <button class="secondary-btn" on:click={() => goto('/skills')}>My Skills</button>
                </div>
            </div>
        </div>
    </section>
</main>

<style>
	main {
		display: flex;
		align-items: center;
		justify-content: center;
		min-height: 80vh;
	}

	.hero {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		text-align: center;
		max-width: 900px;
		opacity: 0;
		transform: translateY(20px);
		transition: opacity 0.8s ease, transform 0.8s ease;
	}

	.hero.visible {
		opacity: 1;
		transform: translateY(0);
	}

	.content-container {
		background: rgba(0, 0, 0, 0.2);
		backdrop-filter: blur(10px);
		border-radius: 24px;
		padding: 4rem 3rem;
		box-shadow: 0 10px 40px rgba(0, 0, 0, 0.2);
		border: 1px solid rgba(255, 255, 255, 0.1);
		width: 100%;
	}

	.text-content {
		max-width: 650px;
		margin: 0 auto;
	}

	h1 {
		font-weight: 700;
		font-size: clamp(3.5rem, 8vw, 5.5rem);
		margin: 0;
		line-height: 1.1;
		background: linear-gradient(90deg, #ffffff, #c5d3ff);
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
		background-clip: text;
		text-fill-color: transparent;
	}

	.tagline {
		font-style: normal;
		font-size: clamp(1.2rem, 3vw, 1.6rem);
		margin: 0.5rem 0 1.5rem;
		color: var(--color-theme-1);
		font-weight: 500;
		letter-spacing: 0.02em;
	}

	.description {
		font-size: 1.15rem;
		margin-bottom: 2.5rem;
		max-width: 600px;
		margin-left: auto;
		margin-right: auto;
		line-height: 1.6;
	}

	.button-container {
		display: flex;
		gap: 1rem;
		justify-content: center;
		flex-wrap: wrap;
	}

	button {
		padding: 1rem 2rem;
		font-size: 1rem;
		font-weight: 500;
		border: none;
		border-radius: 10px;
		cursor: pointer;
		transition: all 0.3s ease;
	}

	.primary-btn {
		background-color: var(--color-theme-1);
		color: white;
	}

	.primary-btn:hover {
		background-color: var(--color-theme-2);
		transform: translateY(-3px);
		box-shadow: 0 6px 20px rgba(0, 0, 0, 0.25);
	}

	.secondary-btn {
		background-color: rgba(255, 255, 255, 0.1);
		color: white;
		border: 1px solid rgba(255, 255, 255, 0.2);
	}

	.secondary-btn:hover {
		background-color: rgba(255, 255, 255, 0.2);
		transform: translateY(-3px);
		box-shadow: 0 6px 20px rgba(0, 0, 0, 0.2);
	}

	@media (max-width: 768px) {
		.content-container {
			padding: 3rem 1.5rem;
		}

		.button-container {
			flex-direction: column;
			width: 100%;
		}

		button {
			width: 100%;
		}
	}
</style>
