<script lang="ts">
	import Icon from '@iconify/svelte';
	import BreadCrumb from '../../../components/shared/BreadCrumb.svelte';
	import ProfileTab from '../../../components/cards/patient/patient-tabs/ProfileTab.svelte';
	import CommunitiesTab from '../../../components/cards/patient/patient-tabs/CommunitiesTab.svelte';
	import PatientContact from '../../../components/cards/patient/patient-tabs/PatientContact.svelte';
	import PatientSettingTab from '../../../components/cards/patient/patient-tabs/PatientSettingTab.svelte';

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
		<section class="community-card">
			<div class="flex flex-wrap items-center gap-3">
				<a href={`/communities/1`} class="relative h-12 w-12">
					<img src={`https://source.boringavatars.com/pixel`} alt={`community.name`} class="rounded-full object-cover" />
				</a>
				<div>
					<a href={`/communities/1`} class="inline-flex items-center">
						<h4 class="text-base-semibold text-light-1">{`KNH Community group`}</h4> 
						<span class="pl-1 text-gold rounded-full float-right">
						<Icon icon="ic:round-verified" class="w-5 h-5" />
						</span>
					</a>
					<p class="text-small-medium text-gray-1">@{`kenyattacom`}</p>
				</div>
			</div>
			<p class="mt-4 text-subtle-medium text-gray-1">{`Kenyatta National HIV community help groups.`}</p>
			<div class="mt-5 flex flex-wrap items-center justify-start gap-3">
				<span class="button-icon">
					<Icon icon="mdi:show" height="20" />
				</span>
				<span class="button-icon">
					<Icon icon="material-symbols:share" height="20" />
				</span>
			</div>
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
