<script lang="ts">
	type VideoProps = {
		video: string;
	};

	const { video }: VideoProps = $props();
</script>

<div class="flex justify-center">
	<video class="rounded-xl" controls loop width="700">
		<source src={video} />
	</video>
</div>
