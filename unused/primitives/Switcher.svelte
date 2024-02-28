<script lang="ts">
	// A CSS width value (representing the 'container breakpoint')
	export let threshold = 'var(--measure)';
	// A CSS margin value
	export let space = 'var(--s1)';
	// A number representing the maximum number of items permitted for a horizontal layout
	export const limit = 4;
</script>

<div class="switcher" style="--gutter: {space}; --threshold: {threshold}">
	<slot />
</div>

<style>
	.switcher {
		display: flex;
		flex-wrap: wrap;
		/* The default value is the first point on the modular scale */
		gap: var(--gutter, var(--s1));

		& > * {
			/* Allow children to grow */
			flex-grow: 1;
			/* Switch the layout at the --threshold (the width at which the layout 'breaks') */
			flex-basis: calc((var(--threshold) - 100%) * 999);
		}

		& > :nth-last-child(n + 5),
		& > :nth-last-child(n + 5) ~ * {
			/* Switch to a vertical configuration if there are more than 4 child elements */
			flex-basis: 100%;
		}
	}
</style>
