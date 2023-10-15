<script lang="ts">
	import Icon from '@iconify/svelte';
	import ProfileCardHeader from '../../../components/cards/profile/ProfileCardHeader.svelte';
	import BreadCrumb from '../../../components/shared/BreadCrumb.svelte';
	import ProfileTab from '../../../components/cards/patient/patient-tabs/ProfileTab.svelte';
	import CommunitiesTab from '../../../components/cards/patient/patient-tabs/CommunitiesTab.svelte';
	import PatientContact from '../../../components/cards/patient/patient-tabs/PatientContact.svelte';
	import PatientSettingTab from '../../../components/cards/patient/patient-tabs/PatientSettingTab.svelte';
	import CommunityCard from '../../../components/cards/community/CommunityCard.svelte';

	let Tabs = [
		{ title: 'Page Info', icon: 'gg:profile', content:ProfileTab },
		{ title: 'Members', icon: 'clarity:group-solid', content: CommunitiesTab },
        { title: 'Posts', icon: 'fluent:contact-card-16-filled', content: PatientContact },
		{ title: 'Settings', icon: 'ic:baseline-settings', content: PatientSettingTab }
		
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
        <CommunityCard />
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
