<script lang="ts">
	import CardWithImage from '../card-with-image/card-with-image.svelte';
	import Circle from './circle.svelte';
	import JobInfo from './job-info.svelte';

	// type Post = {
	// 	image: string;
	// 	title: string;
	// };

	// type CompanyDetail = {
	// 	logo: string;
	// 	name: string;
	// 	location: string;
	// 	position: string;
	// 	timing: string;
	// };

	// type Timeline = {
	// 	time: string;
	// 	isJobTimeline: boolean;
	// 	companyDetails: CompanyDetail[] | null;
	// 	posts?: Post[] | null;
	// };

	const TIMELINE_STORIES = [
		{
			time: 'Dec 2023',
			isJobTimeline: false,
			companyDetails: null,
			posts: [
				{
					image: '/steve-jobs-bg.svg',
					title: 'No amount of technology can convert a bad story into a good story.'
				},
				{
					image: '/sam-bg.svg',
					title:
						"Most people don't have original ideas. Here is how Sam Altman pushes himself to have unpopular ideas."
				}
			]
		},
		{
			time: 'Dec 2023',
			isJobTimeline: true,
			companyDetails: {
				logo: '/logo.svg',
				name: 'Duggup',
				location: 'San Francisco Bay Area',
				position: 'Co-Founder and CEO',
				timing: 'Full-time · Remote'
			},
			posts: null
		},
		{
			time: 'Dec 2023',
			isJobTimeline: false,
			companyDetails: null,
			posts: [
				{
					image: '/pc-bg.svg',
					title: 'Startup Lesson I am reflecting. Don\'t build for the "average person".'
				},
				{
					image: '/map-bg.svg',
					title: 'Your biggest regrets at 80 will be acts of omission.'
				}
			]
		},
		{
			time: 'Sep 2022',
			isJobTimeline: true,
			companyDetails: {
				logo: '/betterup-logo.svg',
				name: 'BetterUp',
				location: 'San Francisco Bay Area',
				position: 'VP Engineering',
				timing: 'Full-time'
			},
			posts: null
		}
	];
	
	let TIMELINE_HEIGHT: number = 100;
	TIMELINE_STORIES.forEach((story) => {
		if (story.isJobTimeline) {
			TIMELINE_HEIGHT += 157;
		} else {
			TIMELINE_HEIGHT += 288;
		}
	});
</script>

<div class={`relative mx-auto h-[${TIMELINE_HEIGHT}px] w-11/12 border-s-4 border-dotted ps-5`}>
	{#each TIMELINE_STORIES as item}
		{#if item.isJobTimeline}
			<div class="relative h-[157px]">
				<Circle isBigCircle={true} styles={`absolute left-[-36px] top-[70px]`} />
				<div class={`absolute left-[-210px] top-[35px]`}>
				<JobInfo companyName={item.companyDetails?.name} logo={item.companyDetails?.logo} timing={item.companyDetails?.timing} location={item.companyDetails?.location}/>
				</div>
				<div class="flex h-full flex-col justify-center ps-3">
					<h3 class="text-xl font-bold text-[#141618]">{item.companyDetails?.position}</h3>
					<span class="text-base font-normal text-[#7A9299]">{item.companyDetails?.timing}</span>
				</div>
			</div>
		{:else}
			<div class="relative h-[288px]">
				<Circle isBigCircle={false} styles="absolute left-[-30px] top-[144px]" />
				<span class={`absolute left-[-110px] top-[140px] text-[#7A9299] text-base font-normal`}>{item.time}</span>
				<div class="flex h-full items-center justify-start gap-6 ps-3">
					{#each item.posts as post}
						<CardWithImage image={post.image} text={post.title} />
					{/each}
				</div>
			</div>
		{/if}
	{/each}
</div>
