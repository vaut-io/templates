<script lang="ts">
	// The element's aspect ratio
	export let ratio = '4:3';


	let splitRatio = ratio.split(':')
</script>

<div class="frame" style="--n: {splitRatio[0]}; --d: {splitRatio[1]}">
	<slot />
</div>

<style>
	.frame {
		/* Numerator and denominator */
		aspect-ratio: var(--n) / var(--d);
		overflow: hidden;
		display: flex;
		justify-content: center;
		align-items: center;
	}
	.frame > img,
	.frame > video {
		inline-size: 100%;
		block-size: 100%;
		object-fit: cover;
	}
</style>
