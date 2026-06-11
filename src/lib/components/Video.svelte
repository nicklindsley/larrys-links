<script lang="ts">
	type VideoProps = {
		video: string;
	};

	const { video }: VideoProps = $props();
</script>

<div class="flex justify-center">
	<video
		class="rounded-xl"
		width="700"
		muted
		controls
		controlslist="nodownload"
		disableremoteplayback
	>
		<source src={video} />
	</video>
</div>
