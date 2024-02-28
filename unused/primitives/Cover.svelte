<script lang="ts">
	// A simple selector such an element or class selector, representing the centered (main) element in the cover
	export let centered = 'h1';
	// The minimum space between and around all of the child elements
	export let space = 'var(--s1)';
	// The minimum height (block-size) for the Cover
	export let minHeight = '100vh';
	// Whether the spacing is also applied as padding to the container element
	export let noPad = false;
</script>

<div class="cover" style="--space: {space}; --min-height: {minHeight}; --selector: {centered}">
	<slot />
</div>

<style>
	.cover {
		/* Establish a columnal flex context */
		display: flex;
		flex-direction: column;
		/* Set a minimum height to match the viewport height (any minimum would be fine) */
		min-block-size: var(--min-height);
		/* Set a padding value */
		padding: var(--space);
	}
	.cover > * {
		/* Give each child a top and bottom margin */
		margin-block: var(--s1);
	}
	.cover > :first-child:not(h1) {
		/* Remove the top margin from the first-child if it _doesn't_ match the centered element */
		margin-block-start: 0;
	}
	.cover > :last-child:not(h1) {
		/* Remove the bottom margin from the last-child if it _doesn't_ match the centered element */
		margin-block-end: 0;
	}
	.cover > h1 {
		/* Center the centered element (h1 here) in the available vertical space */
		margin-block: auto;
	}
</style>
