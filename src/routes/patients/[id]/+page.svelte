<script lang="ts">
	import Icon from '@iconify/svelte';
	import ProfileCardHeader from '../../../components/cards/profile/ProfileCardHeader.svelte';
	import BreadCrumb from '../../../components/shared/BreadCrumb.svelte';
	import ProfileTab from '../../../components/cards/patient/patient-tabs/ProfileTab.svelte';
	import CommunitiesTab from '../../../components/cards/patient/patient-tabs/CommunitiesTab.svelte';
	import PatientSettingTab from '../../../components/cards/patient/patient-tabs/PatientSettingTab.svelte';
	import { Patients } from '../../../data/SomeData';

	let Tabs = [
		{ title: 'Profile', icon: 'gg:profile', content: ProfileTab },
		{ title: 'Communities', icon: 'clarity:group-solid', content: CommunitiesTab },
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
			parentName="Patients"
			parentLink="/patients"
			childName="Virginia Kring"
		/>
	</div>
	<div>
		{#each Patients.slice(0, 1) as patient}
			<ProfileCardHeader
				profileURL={patient.photoURL}
				firstName={patient.firstName}
				lastName={patient.lastName}
			/>
		{/each}
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
				<div class="text-light-1 py-3">
					<svelte:component this={tab.content} />
						
				</div>
			{/if}
		{/each}
	</div>
</section>
