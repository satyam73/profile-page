<script lang="ts">
	import Button from '$lib/components/ui/button/button.svelte';
	import NavLink from './nav-link.svelte';
	type NavbarLink = {
		id: string;
		text: string;
		link: string;
		icon: string;
	};

	const USERNAME = 'Krishna Kiran';

	const NAVBAR_LINKS: NavbarLink[] = [
		{
			id: 'home',
			text: 'Home',
			link: '/',
			icon: '/icons/home.svg'
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

<header class="flex items-center justify-between border-b border-dashed px-2 py-4">
	<a href="/">
		<span class="logo flex items-center gap-1">
			<img src="/logo.svg" class="w-10" alt="Duggup" />
			<span class="text-3xl font-bold text-[#333333]"> Duggup </span>
		</span>
	</a>
	<nav class="link flex items-center gap-7">
		{#each NAVBAR_LINKS as item}
			<NavLink
				icon={item.icon}
				text={item.text}
				id={item.id}
				link={item.link}
				styles={'max-lg:hidden'}
			/>
		{/each}
		<Button
			variant="outline"
			class="ml-2 border border-b-4 border-[#4D4D4D] text-sm font-normal text-[#4D4D4D] max-lg:hidden"
		>
			<img src="/icons/plus-square.svg" class="mr-2 h-4 w-4" alt="plus square" />
			Post
		</Button>
		<span class="flex items-center">
			<Button variant="ghost" class="gap-3	text-xl	font-medium hover:bg-transparent">
				<img class="rounded-full border border-[#4D4D4D]" src="/user-image.svg" alt={USERNAME} />
				{USERNAME}
				<img src="/icons/chevron-down.svg" alt="chevron down" />
			</Button>
		</span>
	</nav>
</header>
