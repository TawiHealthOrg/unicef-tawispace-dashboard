<script lang="ts">
import Icon from '@iconify/svelte';
	import ProfileImage from '../../../lib/images/assets/images/profile1.jpg';
	import { goto } from '$app/navigation';
    export let name:string,username:string,bio:string;
</script>

<div class="caregiver-card">
	<div class="user-card_avatar">
		<img src={ProfileImage} alt="profile" width={48} height={48} class="rounded-full" />
		<div class="flex-1 text-ellipsis">
			<h4 class="text-base-semibold text-light-1">{name}</h4>
			<p class="text-small-medium text-gray-1">@{username}</p>
		</div>
	</div>
    <div>
        <p class="mt-2 text-subtle-medium text-gray-1">{bio}</p>
    </div>
	<div class="flex gap-3">
		<button class="button-icon" on:click={() =>goto('/care-givers')}>
			<Icon icon="mdi:show" height="20" />
		</button>
		<button class="button-icon">
			<Icon icon="ic:baseline-email" height="20" />
		</button>
		<button class="button-icon" on:click={() =>goto('/care-givers')}>
			<Icon icon="ion:calendar" height="20" />
		</button>
		<button class="button-icon">
			<Icon icon="carbon:video-filled" height="20" />
		</button>
	</div>
</div>