<script lang="ts">
	import ApiShowcase from '../lib/components/ApiShowcase.svelte';
	import CssShowcase from '../lib/components/CssShowcase.svelte';
</script>

<div class="outer">
	<div class="titleText">
		<h1>You landed in</h1>
		<h1 class="nowrap">
			<p>T3</p>
			<h1 class="svelteFont">SVELTEKIT</h1>
		</h1>
	</div>
	<div class="inner">
		<ApiShowcase />
		<CssShowcase />
	</div>
</div>

<style>
	.outer {
		display: flex;
		flex-direction: column;
		align-items: center;
		text-align: center;
		gap: 7rem 0px;
	}

	.nowrap {
		display: flex;
		flex-direction: row;
		flex-wrap: nowrap;
		align-items: center;
	}

	.titleText {
		padding-top: 50px;
		font-size: 2rem;
		line-height: 2rem;
	}
	.svelteFont {
		font-family: 'Overpass', sans-serif;
		font-size: 5rem;
	}

	.inner {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		text-align: center;
		gap: 5rem 0px;
	}
</style>
