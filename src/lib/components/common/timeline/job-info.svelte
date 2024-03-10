<script lang="ts">
	export let companyName: string = '';
	export let location: string = '';
	export let placeholder: string = 'Joined';
	export let timing: string = '';
	export let logo: string = '/logo.svg';

	const fontClass = 'font-normal text-base text-[#7A9299] leading-[130%]';
</script>

<div class="flex flex-col items-end">
	<img src={logo} alt={companyName} class="h-12 w-12" />
	<span class={fontClass}>{companyName}</span>
	<span class={fontClass}>{location}</span>
	<span class={fontClass}>{placeholder}</span>
	<span class={fontClass}>{timing}</span>
</div>
