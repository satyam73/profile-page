<script lang="ts">
	export let image: string;
	export let text: string;
	export let link: string = 'https://google.com';
</script>

<a href={link} target="_blank">
	<div class="h-[226px] w-[344px] overflow-hidden rounded-xl border">
		<img class="h-[136px] w-full object-cover" src={image} alt="" />
		<div class="flex h-[90px] items-center px-3 text-sm font-normal text-[#141618]">
			<div class="line-clamp-2 h-[41px]">
				{text}
			</div>
		</div>
	</div>
</a>
