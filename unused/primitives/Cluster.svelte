<script lang="ts">
	export let list = false;

	// A CSS justify-content value
	export let justify = 'flex-start';

	// A CSS align-items value
	export let align = 'flex-start';

	// A CSS gap value. The minimum space between the clustered child elements.
	export let space = 'var(--s1)';
</script>

<svelte:element
	this={list ? 'ul' : 'div'}
	style="--justify: {justify}; --align: {align}; --space: {space}"
>
	<slot />
</svelte:element>

<style>
	div,
	ul {
		/* Set the Flexbox context */
		display: flex;
		/* Enable wrapping */
		flex-wrap: wrap;
		/* Set the space/gap */
		gap: var(--space, 1rem);
		/* Choose your justification (flex-start is default) */
		justify-content: var(--justify);
		/* Choose your alignment (flex-start is default) */
		align-items: var(--align);
	}
</style>
