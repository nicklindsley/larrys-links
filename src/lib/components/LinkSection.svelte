<script lang="ts">
	import Link from '$lib/components/Link.svelte';
	import Video from '$lib/components/Video.svelte';
	import type { ComponentProps } from 'svelte';

	type LinkProps = ComponentProps<typeof Link> & ComponentProps<typeof Video>;

	const props: LinkProps = $props();
</script>

<div class="col-span-2 grid grid-cols-subgrid gap-5">
	<Link {...props} />
	{#if props.video}
		<Video video={props.video} />
	{/if}
</div>
