<script lang="ts">
	import Link from '$lib/components/Link.svelte';
	import type { ComponentProps } from 'svelte';

	type LinkProps = {
		title: string;
		links: ComponentProps<typeof Link>[];
	};

	const { title, links }: LinkProps = $props();
</script>

<div class="flex flex-col gap-3">
	<h4>{title}</h4>
	<div class="flex flex-col gap-3">
		{#each links as link (link.name)}
			<Link {...link} />
		{/each}
	</div>
</div>
