<script lang="ts">
	export let image: string | null = '';
	export let text: string | null = '';
	export let link: string = 'https://google.com';
</script>

<a href={link} target="_blank">
	<div
		class="h-[226px] w-[344px] overflow-hidden rounded-xl border max-xl:h-[176px] max-xl:w-[294px] max-sm:max-w-[80%]"
	>
		<img class="w-full object-cover max-xl:h-[106px] xl:h-[136px]" src={image} alt="" />
		<div
			class="flex items-center px-3 text-sm font-normal text-[#141618] max-xl:h-[70px] xl:h-[90px]"
		>
			<div class="line-clamp-2 h-[41px]">
				{text}
			</div>
		</div>
	</div>
</a>
