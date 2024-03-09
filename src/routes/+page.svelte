<script lang="ts">
	import CardWithImage from '$lib/components/common/card-with-image/card-with-image.svelte';
	import ProfileHeader from '$lib/components/profile-header/profile-header.svelte';
  
</script>

<div>
	<ProfileHeader />

  <CardWithImage image={'/steve-jobs-bg.svg'} text={'No amount of technology can convert a bad story into a good story.'}/>
</div>
