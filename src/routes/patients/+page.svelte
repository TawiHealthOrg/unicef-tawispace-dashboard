<script lang="ts">
	import SearchCard from "../../components/cards/patient/SearchCard.svelte";
	import PatientCard from "../../components/cards/patient/PatientCard.svelte";
	import Icon from "@iconify/svelte";
</script>

<section>
    <div class="flex justify-between">
        <h1 class='text-heading4-medium text-light-1'>Patients</h1>
        <button class="button-icon text-small-regular bg-gradient-to-tr from-greenPrimary to-primary max-xs:hidden">Add patient</button>
        <button class="button-icon text-small-regular bg-gradient-to-tr from-greenPrimary to-primary xs:hidden"><Icon icon="material-symbols:add" height="24" /></button>
    </div>
    <div class="mt-5">
        <SearchCard />
    </div>
    <div class="mt-10 flex flex-col gap-5">
        <PatientCard />
    </div>
</section>