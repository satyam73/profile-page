<script lang="ts">
	import Timeline from '$lib/components/common/timeline/timeline.svelte';
	import ProfileHeader from '$lib/components/profile-header/profile-header.svelte';
</script>

<svelte:head>
	<title>Duggup | Profile</title>
</svelte:head>
<div class="flex flex-col gap-4 max-xl:gap-10">
	<ProfileHeader />
	<Timeline />
</div>
