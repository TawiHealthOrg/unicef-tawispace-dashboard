<script>
	import Counter from './Counter.svelte';
	import welcome from '$lib/images/svelte-welcome.webp';
	import welcome_fallback from '$lib/images/svelte-welcome.png';
	import Icon from '@iconify/svelte';
</script>

<svelte:head>
	<title>Tawispace</title>
	<meta name="description" content="Tawispace platform for adolescents living with HIV/AIDS Sexual and Reproductive Health Challenges" />
</svelte:head>

<h4 class="text-heading4-medium text-light-1 text-left">Welcome, <span class="">{`John!`}</span></h4>
<section class="mt-9 flex flex-col sm:flex-row gap-4">
  <div class="dashboard-card">
	<div class="flex flex-wrap items-center gap-3">
	  <span class="p-3 text-light-1 rounded-full bg-greenPrimary"><Icon icon="mdi:patient-outline" height={24} /></span>
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
	  <span class="p-3 text-light-1 rounded-full bg-greenPrimary"><Icon icon="clarity:group-solid" height={24} /></span>
	  <div>
		<a href={`/communities`}>
		  <h4 class="text-base-semibold text-light-1">{`Community Groups`}</h4>
		</a>
		<p class="text-small-medium text-gray-1">{`community groups registered`}</p>
	  </div>
	</div>
	<p class="mt-4 text-subtle-medium text-gray-1">{`Community group for KNH for Nairobi HIV`}</p>
	<div class="mt-5 flex flex-wrap items-center justify-between gap-3">
	  
	</div>
  </div>
</section>
<section class="mt-9 grid grid-col-1 w-full">
  <div class="w-full rounded-lg bg-dark-3 px-4 py-5 h-full ">
	<div class="flex flex-wrap items-center gap-3">
	  <div class="border-b pb-3 border-white">
		<h4 class="text-base-semibold text-light-1">{`KNH Community Group`}</h4>
		<p class="text-small-medium text-gray-1">@{`knhcomms`}</p>
	  </div>
	</div>
	<p class="mt-4 text-subtle-medium text-gray-1">{`Community group for KNH for Nairobi HIV`}</p>
	<div class="mt-5 flex flex-wrap items-center justify-between gap-3">
	  
	</div>
  </div>
</section>
<section class="mt-9 grid grid-col-1 w-full max-h-fit">
  <div class="w-full rounded-lg bg-dark-3 px-4 py-5 h-full ">
	<div class="flex flex-wrap items-center gap-3">
	  <div class="border-b pb-3 border-white">
		<h4 class="text-base-semibold text-light-1">{`Statistics here`}</h4>
	  </div>
	</div>
	<p class="mt-4 text-subtle-medium text-gray-1">{`Community group for KNH for Nairobi HIV`}</p>
	<div class="mt-5 flex flex-wrap items-center justify-between gap-3">
	  
	</div>
  </div>
</section>
