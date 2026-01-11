<script lang="ts">
	type LinkProps = {
		name: string;
		url: string;
		faviconUrl?: string;
	};

	const { name, url, faviconUrl = url }: LinkProps = $props();

	const faviconSize = 24;
	const favicon = $derived(
		`https://www.google.com/s2/favicons?domain=${encodeURIComponent(faviconUrl)}&sz=${faviconSize}`
	);
</script>

<div class="ml-5 flex gap-1">
	<img src={favicon} alt={name} width={faviconSize} />
	<!-- eslint-disable-next-line svelte/no-navigation-without-resolve -->
	<a class="text-blue-600 underline" href={url} target="_blank" rel="noopener noreferrer">
		{name}
	</a>
</div>
