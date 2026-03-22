<script lang="ts">
	import "../index.css";
	import favicon from "$lib/assets/favicon.ico";

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

<h1 class="title page-title">metaKGP <span class="accent">Atlas</span></h1>
{@render children()}
