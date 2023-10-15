<script>
	import { goto } from "$app/navigation";
	import Icon from "@iconify/svelte";
	import SearchCard from "../../components/cards/patient/SearchCard.svelte";
	import CaregiverCard from "../../components/cards/caregiver/CaregiverCard.svelte";

</script>
<div class="flex justify-between">
    <h1 class="text-heading4-medium text-light-1">Caregivers</h1>
    <button
        on:click={()=> goto('/patients/add')}
        class="button-icon text-small-regular bg-gradient-to-tr from-greenPrimary to-primary max-xs:hidden"
        >Add caregivers</button
    >
    <button
        class="button-icon text-small-regular bg-gradient-to-tr from-greenPrimary to-primary xs:hidden"
        ><Icon icon="material-symbols:add" height="24" /></button
    >
</div>
<div class="mt-5">
    <SearchCard 
    inputPlaceholder="Search caregivers"
    />
</div>
<div class="mt-10 grid lg:grid-cols-3 md:grid-cols-3 sm:grid-cols-2 gap-5">
    <CaregiverCard name="John Doe" username="johndoe" bio="special diet is required or special food preparations. "/>
    <CaregiverCard name="Jane Doe" username="janedoe" bio="special diet is required or special food preparations. "/>
    <CaregiverCard name="James Doe" username="jamesdoe" bio="special diet is required or special food preparations. "/>
    <CaregiverCard name="Joy Doe" username="joydoe" bio="special diet is required or special food preparations. "/>
   
</div>