<script lang="ts">
	import Timeline from '$lib/components/common/timeline/timeline.svelte';
	import ProfileHeader from '$lib/components/profile-header/profile-header.svelte';
</script>

<div class="flex flex-col gap-4">
	<ProfileHeader />
	<!-- <div class="h-[100vh] bg-slate-400" >
		color
	</div> -->
	<!-- <div class="w-full overflow-auto "> -->
	<Timeline />
	<!-- </div> -->
</div>
