<script lang="ts">
	  export let icon :string;
		export let text :string;
		export let link :string;
		export let id :string;
</script>

<a class="text-[#4D4D4D] flex text-sm items-center gap-1" href={link}>
	<img src={icon} alt={id} />
	<span>{text} </span>
</a>
