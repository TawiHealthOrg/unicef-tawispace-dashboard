<script lang="ts">
	import { goto } from '$app/navigation';
	import Icon from '@iconify/svelte';
	import SearchCard from '../../components/cards/patient/SearchCard.svelte';
	import CaregiverCard from '../../components/cards/caregiver/CaregiverCard.svelte';
	import { Caregivers } from '../../data/SomeData'
</script>

<div class="flex justify-between">
	<h1 class="text-heading4-medium text-light-1">Caregivers</h1>
	<button
		on:click={() => goto('/patients/add')}
		class="button-icon text-small-regular inline-flex items-center gap-1 bg-gradient-to-tr from-greenPrimary to-primary max-xs:hidden"
		><Icon icon="icon-park-solid:add" /> caregivers</button
	>
	<button
		class="button-icon text-small-regular bg-gradient-to-tr from-greenPrimary to-primary xs:hidden"
		><Icon icon="material-symbols:add" height="24" /></button
	>
</div>
<div class="mt-5">
	<SearchCard inputPlaceholder="Search caregivers" />
</div>
<div class="mt-10 grid lg:grid-cols-3 md:grid-cols-3 sm:grid-cols-2 gap-5">
	{#each Caregivers as caregiver}
		<CaregiverCard
			{...caregiver}
		/>
	{/each}
</div>
