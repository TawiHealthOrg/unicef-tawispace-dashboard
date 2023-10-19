<script lang="ts">
	import { goto } from "$app/navigation";
	import Icon from "@iconify/svelte";
	import { Patients } from "../../../../data/SomeData";
</script>
<section class="text-light-1 dashboard-card w-full">
    {#each Patients.slice(0,3) as patient}
        <article class="user-card gap-2 py-2 border-b-2 border-dark-4">
            <a href="/communities/1" class=" hover:cursor-pointer">
                <div class="user-card_avatar">
                    <img src={patient.photoURL} alt={patient.firstName} class="rounded-full w-8 h-8" />
                    <div class="flex-1 text-ellipsis">
                        <h4 class="text-small-medium text-light-1">{`${patient.firstName} ${patient.lastName}`}</h4>
                        <p class="text-small-medium text-gray-1">@{patient.firstName.toLocaleLowerCase()}</p>
                    </div>
                </div>
            </a>
            <div class="flex gap-3.5">
                <button class="button-icon" on:click={() =>goto('/community/1')}>
                    <Icon icon="mdi:show" height="20" />
                </button>
                <button class="button-icon">
                    <Icon icon="gridicons:chat" height="20" />
                </button>
                <button class="button-icon" on:click={() =>goto('/patients/appointment')}>
                    <Icon icon="icomoon-free:reply" height="20" />
                </button>
            </div>
        </article>
    {/each}
    
</section>