<script lang="ts">
	import Icon from "@iconify/svelte";
	import { Patients } from "../../../../data/SomeData";
</script>

<section class="text-light-1 dashboard-card w-full">
    {#each Patients.slice(0, 1)  as patient}
    <div class="grid md:grid-cols-2 gap-4">
        <div class="">
            <h2 class="text-small-medium">Profile Information</h2>  
            <div class="my-4 grid space-y-2">
                <h5 class="text-small-regular inline-flex items-center gap-2"><Icon icon="mdi:user" class="w-5 h-5" />:  <span class="">{`${patient.firstName} ${patient.lastName}`}</span></h5>
                <h5 class="text-small-regular inline-flex items-center gap-2"><Icon icon="ic:baseline-email" class="w-5 h-5" />:  <span class="">{`${patient.emailAddress}`}</span></h5>
                <h5 class="text-small-regular inline-flex items-center gap-2"><Icon icon="ic:baseline-phone" class="w-5 h-5" />: <span class="">{`${patient.phoneNumber}`}</span></h5>
            </div>    
        </div>
        <div class="">
            <h2 class="text-small-medium">Address Information</h2>  
            <div class="my-4 grid space-y-2">
                <h5 class="text-small-regular inline-flex items-center gap-2"><Icon icon="gis:search-country" class="w-5 h-5" />:  <span class="">{`${patient.country}`}</span></h5>
                <h5 class="text-small-regular inline-flex items-center gap-2"><Icon icon="uiw:date" class="w-5 h-5" />:  <span class="">{`${patient.yearOfBirth}`}</span></h5>
                <h5 class="text-small-regular inline-flex items-center gap-2"><Icon icon="icons8:gender" class="w-5 h-5" />: <span class="">{`${patient.gender}`}</span></h5>
                <h5 class="text-small-regular inline-flex items-center gap-2"><Icon icon="healthicons:blood-bag-negative" class="w-5 h-5" />: <span class="">{`${patient.bloodType}`}</span></h5>
            </div>    
        </div>
    </div>
    {/each}
</section>