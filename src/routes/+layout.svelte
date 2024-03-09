<script>
	import Navbar from '$lib/components/common/navbar/navbar.svelte';
	import '../app.pcss';
</script>

<div class="mx-auto max-w-[1424px]">
	<Navbar />
	<div class="mx-auto max-w-[1024px] pt-10">
		<slot />
	</div>
</div>
