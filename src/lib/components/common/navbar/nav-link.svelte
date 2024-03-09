<script lang="ts">
	export let icon: string;
	export let text: string;
	export let link: string;
	export let id: string;
</script>

<a class="flex items-center gap-1 text-sm text-[#4D4D4D]" href={link}>
	<img src={icon} alt={id} />
	<span>{text} </span>
</a>
