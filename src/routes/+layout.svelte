<script lang="ts">
	import './layout.css';
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();
</script>

<svelte:head>
	<title>Larry's Links</title>
	<meta property="og:image" content={favicon} />
	<meta property="og:image:width" content="580" />
	<meta property="og:image:height" content="580" />
	<link rel="icon" href={favicon} />
</svelte:head>
{@render children()}
