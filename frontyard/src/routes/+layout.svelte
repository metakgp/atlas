<script lang="ts">
	import "../index.css";
	import favicon from "$lib/assets/favicon.ico";

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

<div class="page-title">
	<h1 class="title">metaKGP <span class="accent">Atlas</span></h1>
</div>
{@render children()}

<style>
	.page-title {
		width: 100%;

		.title {
			text-align: center;
			font-size: 3rem;
		}
	}
</style>
