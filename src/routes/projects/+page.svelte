<script>
	import TitleReveal from '$lib/TitleReveal.svelte';
</script>

<svelte:head>
	<title>Work | Nick Quam</title>
	<meta
		name="description"
		content="Selected work from Nick Quam, including Checkout and Astretto."
	/>
</svelte:head>

<section class="section">
	<div class="section-heading reveal">
		<p class="card-kicker">Selected work</p>
		<TitleReveal
			lines={['Software with', { text: 'a strong point of view.', className: 'gradient-text' }]}
			yOffset={26}
		/>
		<p>
			I care about the full system: interface, data model, release flow, support surface, and the
			tiny interactions people feel but rarely name.
		</p>
	</div>

	<div class="grid">
		<article class="card checkout-card reveal delay-1">
			<p class="card-kicker">iPhone app</p>
			<h2>Checkout</h2>
			<p>
				Grocery shopping, but smarter. Scan products, rank categories, and see what is actually
				worth putting in your cart.
			</p>
			<div class="tags">
				<span class="tag">SwiftUI</span>
				<span class="tag">Supabase</span>
				<span class="tag">Vision</span>
				<span class="tag">App Store</span>
			</div>
			<a class="card-link" href="https://checkoutrankings.com" target="_blank" rel="noreferrer">
				Open site <span aria-hidden="true">-&gt;</span>
			</a>
		</article>

		<article class="card astretto-card reveal delay-2">
			<p class="card-kicker">Product company</p>
			<h2>Astretto</h2>
			<p>
				A small software studio focused on practical, polished consumer tools that feel native to
				the devices people already love.
			</p>
			<div class="tags">
				<span class="tag">Brand</span>
				<span class="tag">Frontend</span>
				<span class="tag">Motion</span>
				<span class="tag">Launch</span>
			</div>
			<a class="card-link" href="https://astretto.com" target="_blank" rel="noreferrer">
				Open site <span aria-hidden="true">-&gt;</span>
			</a>
		</article>
	</div>
</section>
