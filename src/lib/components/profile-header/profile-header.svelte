<script lang="ts">
	import Button from '$lib/components/ui/button/button.svelte';

	const BIO = `Co-Founder and CEO at Duggup - Social network for people in tech. Ex-Amazon Head of Engineering. I write hot-takes on building a business, shipping delightful products and accelerating product and career growth.`;
	const COMPANY_NAME = 'Duggup';
	const POSITION = 'Co-Founder and CEO';
	const WEBSITE_LINK = 'https://google.com';
</script>

<div class="flex gap-6">
	<div class="profile flex flex-col items-center">
		<img src="/user-image.svg" alt="" class="w-[120px] rounded-full border" />
		<span class="w-24 text-center text-2xl font-bold"> Krishna Kiran </span>
	</div>
	<div class="flex flex-1 flex-col justify-around">
		<p class="bio text=[#141618] text-sm font-normal">
			{BIO}
		</p>
		<Button
			variant="outline"
			class="w-[107px] border border-b-4 border-[#4D4D4D] text-sm font-normal text-[#4D4D4D]"
		>
			Follow
		</Button>
	</div>
	<div class="flex flex-col items-end justify-around">
		<div class="flex flex-col items-end justify-between">
			<img class="h-9 w-9" src="/logo.svg" alt="" />
			<span class="text-base font-bold">{COMPANY_NAME}</span>
			<span class="text=[#7A9299] text-xs font-normal">{POSITION}</span>
		</div>
		<div class="flex">
			<a href={WEBSITE_LINK} class="flex items-center gap-2 text-[#4D4D4D]">
				My website
				<img src="/icons/links-external.svg" alt="" class="mr-1" />
			</a>

			<Button variant="outline" size="icon" class="border-0 hover:bg-transparent">
				<img src="/icons/shortcut.svg" alt="" />
			</Button>
		</div>
	</div>
</div>
