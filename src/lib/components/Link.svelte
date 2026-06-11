<script lang="ts">
	/* eslint-disable svelte/no-navigation-without-resolve */

	type LinkProps = {
		name: string;
		url: string;
		faviconUrl?: string;
		instructions?: string[];
	};

	const { name, url, faviconUrl = url, instructions = [] }: LinkProps = $props();

	const faviconSize = 30;
	const favicon = $derived(
		`https://www.google.com/s2/favicons?domain=${encodeURIComponent(faviconUrl)}&sz=${faviconSize}`
	);
</script>

<div class="ml-5 flex max-w-md flex-col gap-5">
	<div class="flex gap-1">
		<img src={favicon} alt={name} width={faviconSize} />
		<a
			class="text-2xl text-blue-600 underline"
			href={url}
			target="_blank"
			rel="noopener noreferrer"
		>
			{name}
		</a>
	</div>
	{#if instructions.length}
		<div class="flex flex-col gap-1">
			<strong>Login Instructions</strong>
			<ol class="ml-5 list-decimal">
				{#each instructions as instruction, index (index)}
					<li>{instruction}</li>
				{/each}
			</ol>
		</div>
	{/if}
</div>
