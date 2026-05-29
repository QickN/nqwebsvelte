<script>
	/**
	 * @typedef {'h1' | 'h2' | 'h3' | 'h4'} HeadingTag
	 * @typedef {string | { text: string; className?: string }} SourceLine
	 * @typedef {{ text: string; className: string }} NormalizedLine
	 */

	/** @type {HeadingTag} */
	export let as = 'h1';
	/** @type {SourceLine[]} */
	export let lines = [];
	export let className = '';
	/** @type {string | undefined} */
	export let id = undefined;
	export let delayMs = 0;
	export let lineDelayMs = 80;
	export let stepMs = 18;
	export let yOffset = 14;

	/**
	 * @param {SourceLine} line
	 * @returns {NormalizedLine}
	 */
	function normalizeLine(line) {
		return typeof line === 'string'
			? { text: line, className: '' }
			: { text: line.text, className: line.className ?? '' };
	}

	/**
	 * @param {SourceLine[]} sourceLines
	 */
	function buildLines(sourceLines) {
		let charIndex = 0;

		return sourceLines.map((sourceLine, lineIndex) => {
			const line = normalizeLine(sourceLine);
			const words = line.text.split(' ').map((word) => ({
				text: word,
				chars: Array.from(word).map((char) => {
					const delay = delayMs + lineIndex * lineDelayMs + charIndex * stepMs;
					charIndex += 1;
					return { char, delay };
				})
			}));

			return { ...line, words };
		});
	}

	$: titleLines = buildLines(lines);
	$: label = lines.map((line) => normalizeLine(line).text).join(' ');
</script>

<svelte:element
	this={as}
	{id}
	aria-label={label}
	class={`title-reveal ${className}`.trim()}
	style={`--title-y: ${yOffset}px`}
>
	{#each titleLines as line}
		<span class={`title-reveal-line ${line.className ?? ''}`.trim()} aria-hidden="true">
			{#each line.words as word, wordIndex}
				<span class="title-reveal-word">
					{#each word.chars as glyph}
						<span class="title-reveal-char" style={`--title-char-delay: ${glyph.delay}ms`}>
							<span class="title-reveal-glyph">{glyph.char}</span>
						</span>
					{/each}
					{#if wordIndex < line.words.length - 1}
						<span class="title-reveal-space"> </span>
					{/if}
				</span>
			{/each}
		</span>
	{/each}
</svelte:element>
