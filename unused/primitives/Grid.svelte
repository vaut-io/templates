<script lang="ts">
	// A CSS length value representing x in minmax(min(x, 100%), 1fr)
	export let min = '20ch';
	// The space between grid cells
	export let space = 'var(--s1)';
</script>

<div class="grid" style="--minimum: {min}">
	<slot />
</div>

<style>
	.grid {
		/* Establish a grid context */
		display: grid;
		/* Set a gap between grid items */
		grid-gap: 1rem;

		/* Enhance with the min() function into multiple columns */
		grid-template-columns: repeat(auto-fit, minmax(min(var(--minimum), 100%), 1fr));
	}
</style>
