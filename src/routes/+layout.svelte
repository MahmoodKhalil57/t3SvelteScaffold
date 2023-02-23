<script lang="ts">
	import '../app.css';
	import { onMount } from 'svelte';
	import { pwaInfo } from 'virtual:pwa-info';
	let ReloadPrompt: any;
	onMount(async () => {
		pwaInfo && (ReloadPrompt = (await import('$lib/ReloadPrompt.svelte')).default);
	});
	$: webManifest = pwaInfo ? pwaInfo.webManifest.linkTag : '';
</script>

/// <reference lib="virtual:pwa-info" />
/// <reference types="virtual:pwa-info" />

<svelte:head>
	{@html webManifest}
</svelte:head>

<main>
	<slot />
</main>

{#if ReloadPrompt}
	<svelte:component this={ReloadPrompt} />
{/if}
