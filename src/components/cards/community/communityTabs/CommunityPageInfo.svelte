<script lang="ts">
	import Icon from "@iconify/svelte";
	import { Communities, Patients } from "../../../../data/SomeData";
</script>

<section class="text-light-1 dashboard-card w-full">
    {#each Communities.slice(0, 1)  as community}
    <div class="grid md:grid-cols-2 gap-4">
        <div class="">
            <h2 class="text-small-medium">Profile Information</h2>  
            <div class="my-4 grid space-y-2">
                <h5 class="text-small-regular inline-flex items-center gap-2"><Icon icon="mdi:user" class="w-5 h-5" />:  <span class="">{community.name}</span></h5>
                <h5 class="text-small-regular inline-flex items-center gap-2"><Icon icon="ic:baseline-email" class="w-5 h-5" />:  <span class="">{`${community.phoneNumber}`}</span></h5>
                <h5 class="text-small-regular inline-flex items-center gap-2"><Icon icon="ic:baseline-phone" class="w-5 h-5" />: <span class="">{`${community.phoneNumber}`}</span></h5>
            </div>    
        </div>
        <div class="">
            <h2 class="text-small-medium">Address Information</h2>  
            <div class="my-4 grid space-y-2">
                <h5 class="text-small-regular inline-flex items-center gap-2"><Icon icon="bxs:map" class="w-5 h-5" />:  <span class="">{`${community.location}, ${community.postalAddress}`}</span></h5>
            </div>    
        </div>
    </div>
    {/each}
</section>