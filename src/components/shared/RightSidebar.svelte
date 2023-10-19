<script lang="ts">
	import Icon from '@iconify/svelte';
	import { Communities } from '../../data/SomeData'
	import SectionAge from '../dashboard/Section-Age.svelte';
	import SectionCounties from '../dashboard/Section-Counties.svelte';

</script>

<section class="custom-scrollbar rightsidebar">
    <div class="flex flex-1 flex-col justify-start">
        <h3 class=" text-light-1 inline-flex items-center gap-1 pb-4">Youth Demographic <Icon icon="ph:graph" /></h3>
        <div class="w-full rounded-lg bg-dark-3 px-4 py-5 h-full ">
            <div class="flex flex-wrap items-center gap-3">
               <SectionAge />
            </div>
        </div>
    </div>
    <div class="flex flex-1 flex-col justify-start">
        <h3 class="text-light-1 inline-flex items-center gap-1">New communities <Icon icon="clarity:group-solid" /></h3>
        <p class=" text-subtle-medium text-gray-1 mb-3">Lastest Registered communities</p>
        <div class="w-full rounded-lg space-y-1 bg-dark-3 px-2 py-3 h-full border-b-4">
            {#each Communities.slice(0,3) as community}
                <div title={community.name} class="flex flex-wrap hover:cursor-pointer shadow-xl p-2 bg-gray-900 hover:bg-gray-800 transition-all duration-300 rounded items-center gap-3">
                    <article class="user-card ">
                        <div class="user-card_avatar">
                            <img src={community.photoURL} alt="ii" width={30} height={30} class="rounded-full" />
                            <div class="flex-1 text-ellipsis">
                                <h4 class="text-base-medium text-light-1">{community.name.split(/\s+./)[0]}
                                    {#if community.verified}
                                        <span class="text-gold rounded-full inline-flex">
                                            <Icon icon="ic:round-verified" class="w-3 h-3" />
                                        </span>
                                    {/if}
                                    <!-- <span class="relative flex h-3 w-3">
                                        <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-sky-400 opacity-75"></span>
                                        <span class="relative inline-flex rounded-full h-3 w-3 bg-sky-500"></span>
                                    </span> -->
                                </h4>
                                <p class="text-small-regular text-gray-1">@{community.username}</p>
                            </div>
                        </div>
                    </article>
                </div>
            {/each}

            <div class="py-4 text-center">
                <a href="/communities" class="text-light-1 text-base-regular inline-flex items-center gap-1 p-2 bg-gray-700 rounded hover:bg-gray-900 transition-all duration-300 hover:scale-105"><Icon icon="carbon:view-filled" /> more</a>
            </div>
        </div>
        
    </div>
</section>