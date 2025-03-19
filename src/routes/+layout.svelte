<script>
	import { dev } from "$app/environment";
</script>

<svelte:head>
	{#if !dev}
		<link href="/pagefind/pagefind-ui.css" rel="stylesheet" />
		<script src="/pagefind/pagefind-ui.js"></script>
		<script>
			window.addEventListener('DOMContentLoaded', (event) => {
				new PagefindUI({ element: '#search', showSubResults: true });
			});
		</script>
	{/if}
</svelte:head>

<div id="search"></div>

<slot></slot>
