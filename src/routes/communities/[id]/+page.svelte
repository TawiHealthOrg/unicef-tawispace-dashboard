<script lang="ts">
	import Icon from '@iconify/svelte';
	import BreadCrumb from '../../../components/shared/BreadCrumb.svelte';
	import CommunityPageInfo from '../../../components/cards/community/communityTabs/CommunityPageInfo.svelte';
	import CommunityMembers from '../../../components/cards/community/communityTabs/CommunityMembers.svelte';
	import CommunityPosts from '../../../components/cards/community/communityTabs/CommunityPosts.svelte';
	import { Communities } from '../../../data/SomeData';

	let Tabs = [
		{ title: 'Page Info', icon: 'gg:profile', content:CommunityPageInfo },
		{ title: 'Members', icon: 'clarity:group-solid', content: CommunityMembers },
        { title: 'Activities', icon: 'fluent:shifts-activity-20-filled', content: CommunityPosts },
	];

	let activeTab = Tabs[0].title;
	const setActiveTab = (tabTitle: any) => {
		activeTab = tabTitle;
	};
</script>

<section>
	<div class="mb-2 hidden sm:block">
		<BreadCrumb
			baseLink="/"
			baseName="Tawispace"
			parentName="Communities"
			parentLink="/communities"
			childName="KNH HIV Community"
		/>
	</div>
	<div>
		<section class="community-card">
			{#each Communities.slice(0,1) as community}
			<div class="flex flex-wrap items-center gap-3">
				<a href={`/communities/1`} class="relative h-12 w-12">
					<img src={community.photoURL} alt={community.name} class="rounded-full object-cover" />
				</a>
				<div>
					<a href={`/communities/1`} class="inline-flex items-center">
						<h4 class="text-base-semibold text-light-1">{community.name}</h4> 
						<span class="pl-1 text-gold rounded-full float-right">
						<Icon icon="ic:round-verified" class="w-5 h-5" />
						</span>
					</a>
					<p class="text-small-medium text-gray-1">@{community.username}</p>
				</div>
			</div>
			<p class="mt-4 text-subtle-medium text-gray-1">{community.description}</p>
			<div class="text-gray-1 text-small-regular py-1">
				<span>
					Status: <span class="bg-gray-1 p-1 px-4 text-x-small-semibold text-light-1 rounded-lg">verified</span>
				</span>
			</div>
			<div class="text-gray-1 text-small-regular py-1">
				<span>Visibility: <span class="bg-green-600 p-1 px-4 text-x-small-semibold text-light-1 rounded-lg">Public</span></span>
			</div>
			<div class="mt-5 flex flex-wrap items-center justify-start gap-3">
				<span class="button-icon inline-flex items-center text-small-regular gap-1">
					<Icon icon="mdi:show" height="20" /> change visibility 
				</span>
				<span class="button-icon">
					<Icon icon="material-symbols:share" height="20" />
				</span>
			</div>
			{/each}
		</section>
    </div>
	<div class="mt-9">
		<div class="border-b border-gray-200 dark:border-gray-700">
			<ul
				class="flex flex-wrap -mb-px text-sm font-medium text-center text-gray-500 dark:text-gray-400"
			>
				{#each Tabs as tab (tab.title)}
					<li class="mr-2">
						<a
							href={null}
							class={` ${activeTab === tab.title ? 'active-tab' : 'tabs'}`}
							on:click={() => setActiveTab(tab.title)}
						>
							<Icon icon={tab.icon} class="w-5 h-5 mr-2 text-gray-500 " />
							{tab.title}
						</a>
					</li>
				{/each}
			</ul>
		</div>
		{#each Tabs as tab}
			{#if activeTab === tab.title}
				<div class="text-light-1">
                    <svelte:component this={tab.content}/>
				</div>
			{/if}
		{/each}
	</div>
</section>
