<script lang="ts">
	// Which element to treat as the sidebar (all values but "left" are considered "right")
	export let reverse = false;
	// Represents the width of the sidebar when adjacent. If not set (null) it defaults to the sidebar's content width
	export let sideWidth = '';
	// A CSS percentage value. The minimum width of the content element in the horizontal configuration
	export let contentMin = 50;
	// A CSS margin value representing the space between the two elements
	export let space = 'var(--s1)';
	// Make the adjacent elements adopt their natural height
	export let noStretch = false;
</script>

<div
	class="sidebar"
	class:no-stretch={noStretch}
	class:is-reversed={reverse}
	style="--side-width: {sideWidth}; --gutter: {space}; --content-min: {contentMin}%;"
>
	<slot />
</div>

<style>
	.sidebar {
		display: flex;
		flex-wrap: wrap;
		/* The default value is the first point on the modular scale */
		gap: var(--gutter);

		&.no-stretch {
			align-items: flex-start;
		}

		& > :first-child {
			/* The width when the sidebar _is_ a sidebar */
			flex-basis: var(--side-width);
			flex-grow: 1;
		}

		& > :last-child {
			/* Grow from nothing */
			flex-basis: 0;
			flex-grow: 999;
			/* Wrap when the elements are of equal width */
			min-inline-size: var(--content-min);
		}
	}

	.is-reversed {
		flex-direction: row-reverse;
	}

	/* .side-right {
		& > :last-child {
			flex-basis: var(--side-width);
			flex-grow: 1;
		}

		& > :first-child {
			flex-basis: 0;
			flex-grow: 999;
			min-inline-size: var(--content-min);
		}
	} */
</style>
