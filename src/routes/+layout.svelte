<script>
	import Navbar from '$lib/components/common/navbar/navbar.svelte';
	import BottomNav from '$lib/components/common/bottom-nav/bottom-nav.svelte';

	import '../app.pcss';
</script>

<div class="mx-auto max-w-[1424px]">
	<Navbar />
	<div class="mx-auto mb-20 max-w-[1024px] pt-10">
		<slot />
	</div>
</div>
<BottomNav />
