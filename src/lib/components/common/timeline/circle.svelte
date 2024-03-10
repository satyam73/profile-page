<script lang="ts">
	import { cn } from '$lib/utils';

	export let isBigCircle: boolean;
	export let styles: string = '';
</script>

{#if isBigCircle}
	<span class={cn(`block h-7 w-7 rounded-full border-[9px] border-[#0066FF] ${styles}`)}></span>
{:else}
	<span class={cn(`block h-4 w-4 rounded-full border-[3px] border-[#0066FF] ${styles}`)}></span>
{/if}
