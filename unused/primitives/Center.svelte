<script lang="ts">
	// A CSS max-width value
	export let max = 'var(--measure)';
	// Center align the text too (text-align: center)
	export let andText = false;
	// The minimum space on either side of the content
	export let gutters = '0';
	// Center child elements based on their content width
	export let intrinsic = false;
</script>

<div class:andText class:intrinsic style="--max: {max}; --gutter: {gutters}">
	<slot />
</div>

<style>
	div {
		/* Remove padding from the width calculation */
		box-sizing: content-box;
		/* The maximum width is the maximum measure */
		max-inline-size: var(--max);
		/* Only affect horizontal margins */
		margin-inline: auto;
		/* Apply the minimum horizontal space */
		padding-inline-start: var(--gutter);
		padding-inline-end: var(--gutter);
	}

	.intrinsic {
		display: flex;
		flex-direction: column;
		align-items: center;
	}
</style>
