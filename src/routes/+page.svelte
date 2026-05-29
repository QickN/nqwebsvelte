<script>
	import TitleReveal from '$lib/TitleReveal.svelte';
</script>

<svelte:head>
	<title>Nick Quam | Founder & Product Engineer</title>
	<meta
		name="description"
		content="Nick Quam is the founder and product engineer behind Astretto and Checkout, a native iPhone grocery rankings app."
	/>
	<meta name="theme-color" content="#05070c" />
	<meta property="og:title" content="Nick Quam | Founder & Product Engineer" />
	<meta property="og:description" content="Founder and engineer behind Astretto and Checkout." />
	<meta property="og:type" content="website" />
	<meta property="og:url" content="https://nickquam.com" />
</svelte:head>

<section class="hero">
	<div class="hero-inner">
		<div class="eyebrow reveal">
			<span class="pulse" aria-hidden="true"></span>
			Shipping focused consumer software
		</div>

		<TitleReveal
			lines={['Nick Quam', { text: 'builds software.', className: 'gradient-text' }]}
			yOffset={34}
		/>

		<p class="hero-copy reveal delay-1">
			I build focused consumer software from first sketch to App Store review. Current work is
			centered on Checkout, a native iPhone app for ranking what is actually worth buying.
		</p>

		<div class="actions reveal delay-2">
			<a
				class="button primary"
				href="https://checkoutrankings.com"
				target="_blank"
				rel="noreferrer"
			>
				Open Checkout
			</a>
			<a class="button secondary" href="/projects">See the work</a>
		</div>

		<div class="motion-strip reveal delay-3" aria-hidden="true">
			<div class="ticker-track">
				<span>native iOS</span>
				<span>SwiftUI</span>
				<span>Supabase</span>
				<span>product design</span>
				<span>launch systems</span>
				<span>native iOS</span>
				<span>SwiftUI</span>
				<span>Supabase</span>
				<span>product design</span>
				<span>launch systems</span>
			</div>
		</div>
	</div>
</section>

<section class="section" aria-labelledby="current-work">
	<div class="section-heading reveal">
		<TitleReveal as="h2" id="current-work" lines={['Current work']} />
		<p>Two product surfaces with one operating principle: make the useful thing feel obvious.</p>
	</div>

	<div class="grid">
		<article class="card checkout-card reveal delay-1">
			<p class="card-kicker">Launching now</p>
			<h3>Checkout</h3>
			<p>
				A native iPhone grocery rankings app for scanning products, comparing categories, and
				finding the best pick fast.
			</p>
			<div class="tags">
				<span class="tag">SwiftUI</span>
				<span class="tag">Camera</span>
				<span class="tag">Rankings</span>
				<span class="tag">Supabase</span>
			</div>
			<a class="card-link" href="https://checkoutrankings.com" target="_blank" rel="noreferrer">
				View Checkout <span aria-hidden="true">-&gt;</span>
			</a>
		</article>

		<article class="card astretto-card reveal delay-2">
			<p class="card-kicker">Studio</p>
			<h3>Astretto</h3>
			<p>
				The product home for small, precise apps built around taste, utility, and native
				interaction.
			</p>
			<div class="tags">
				<span class="tag">Product</span>
				<span class="tag">Design</span>
				<span class="tag">Web</span>
				<span class="tag">Systems</span>
			</div>
			<a class="card-link" href="https://astretto.com" target="_blank" rel="noreferrer">
				Visit Astretto <span aria-hidden="true">-&gt;</span>
			</a>
		</article>
	</div>
</section>
