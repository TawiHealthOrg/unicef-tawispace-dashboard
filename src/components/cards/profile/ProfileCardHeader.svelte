<script>
	import Icon from '@iconify/svelte';
    import ProfileImage from '../../../lib/images/assets/images/profile1.jpg'
	import { goto } from '$app/navigation';
</script>
<div class="flex w-full flex-col justify-start">
    <div class="flex items-center justify-between">
        <div class="flex items-center gap-3">
            <div class="relative h-20 w-20 object-cover">
                <img src={ProfileImage} alt="profile " class="rounded-full object-cover shadow-2xl"  />
            </div>
            <div class="flex-1">
                <h2 class="text-light-1 text-left text-heading3-bold">John Doe</h2>
                <p class="text-base-medium text-gray-1">@john</p>
            </div>
        </div> 
    </div>
    <p class="mt-6 max-w-lg text-base-regular text-gray-1">Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptas, aliquam?</p>
    <div class="pt-4">
        <div class="flex gap-3.5">
            <button class="button-icon">
                <Icon icon="ic:baseline-email" height="20" />
            </button>
            <button class="button-icon" on:click={() =>goto('/patients/appointment')}>
                <Icon icon="ion:calendar" height="20" />
            </button>
            <button class="button-icon">
                <Icon icon="carbon:video-filled" height="20" />
            </button>
        </div>
    </div>
    <div class="mt-12 h-0.5 w-full bg-dark-3"/>
</div>