<script lang="ts">
	import { cn } from '$lib/utils';

	export let icon: string;
	export let text: string;
	export let link: string;
	export let id: string;
	export let styles: string = '';
</script>

<a class={cn(`flex items-center gap-1 text-sm text-[#4D4D4D] ${styles}`)} href={link}>
	<img src={icon} alt={id} />
	<span>{text} </span>
</a>
