<script lang="ts">
	const NAVBAR_LINKS = [
		{
			id: 'home',
			text: 'Home',
			link: '/',
			icon: '/icons/home.svg'
		},
		{
			id: 'post',
			text: 'Post',
			link: '/post',
			icon: '/icons/plus-square.svg'
		},
		{
			id: 'explore',
			text: 'Explore',
			link: '/explore',
			icon: '/icons/explore.svg'
		},
		{
			id: 'learn',
			text: 'Learn',
			link: '/learn',
			icon: '/icons/open-book.svg'
		}
	];
</script>

<div
	class="fixed bottom-0 left-0 right-0 z-10 h-16 w-full border-t-2 bg-white shadow-2xl lg:hidden"
>
	<nav class="flex items-center justify-evenly">
		{#each NAVBAR_LINKS as link}
			<a href={link.link}>
				<div class="flex flex-1 flex-col items-center justify-end p-0">
					{#if link.id === 'post'}
						<span class="flex h-10 w-10 items-center justify-center">
							<img src={link.icon} alt={link.id} class="h-7 w-7" />
						</span>
					{:else}
						<img src={link.icon} alt={link.id} class="h-10 w-10" />
					{/if}
					<span class="block w-full text-center">{link.text}</span>
				</div>
			</a>
		{/each}
	</nav>
</div>
