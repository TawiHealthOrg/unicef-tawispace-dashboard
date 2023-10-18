<script lang="ts">
	import Icon from '@iconify/svelte';
	import SectionCounties from '../components/dashboard/Section-Counties.svelte';
	import SectionAge from '../components/dashboard/Section-Age.svelte';
	let date = new Date();
	let hours = date.getHours();
	let greeting: string;
	if (hours < 12) {
		greeting = 'Morning';
	} else if (hours >= 12 && hours <= 17) {
		greeting = 'Afternoon';
	} else if (hours >= 17 && hours <= 24) {
		greeting = 'Evening';
	}
     
    
    </script>

<svelte:head>
	<title>Tawispace</title>
	<meta
		name="description"
		content="Tawispace platform for adolescents living with HIV/AIDS Sexual and Reproductive Health Challenges"
	/>
</svelte:head>

<h4 class="text-heading4-medium text-light-1 text-left">
	Good {greeting}, <span class="">{`Victor!`}</span>
</h4>
<section class="mt-9 flex flex-col sm:flex-row gap-4">
	<div class="dashboard-card">
		<div class="flex flex-wrap items-center gap-3">
			<span class="p-3 text-light-1 rounded-full bg-greenPrimary"
				><Icon icon="mdi:patient-outline" height={24} /></span
			>
			<div>
				<a href={`/patients`}>
					<h4 class="text-base-semibold text-light-1">{`Patients`}</h4>
				</a>
				<p class="text-small-medium text-gray-1">{`Total patient registered`}</p>
			</div>
		</div>
		<p class="mt-4 text-subtle-medium text-gray-1">{`Community group for KNH for Nairobi HIV`}</p>
	</div>
	<div class="dashboard-card">
		<div class="flex flex-wrap items-center gap-3">
			<span class="p-3 text-light-1 rounded-full bg-greenPrimary"
				><Icon icon="clarity:group-solid" height={24} /></span
			>
			<div>
				<a href={`/communities`}>
					<h4 class="text-base-semibold text-light-1">{`Community Groups`}</h4>
				</a>
				<p class="text-small-medium text-gray-1">{`community groups registered`}</p>
			</div>
		</div>
		<p class="mt-4 text-subtle-medium text-gray-1">{`Community group for KNH for Nairobi HIV`}</p>
		<div class="mt-5 flex flex-wrap items-center justify-between gap-3" />
	</div>
</section>
<SectionCounties />
<SectionAge />
