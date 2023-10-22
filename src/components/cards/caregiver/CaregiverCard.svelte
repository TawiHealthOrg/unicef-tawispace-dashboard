<script lang="ts">
	import Icon from '@iconify/svelte';
	import { goto } from '$app/navigation';
	export let firstName: string,
		lastName:string,
		bio: string,
		photoURL: string,
		speciality: string,
		verified: boolean;
</script>

<div class="caregiver-card" >
	<div class="user-card_avatar">
		<img src={photoURL} alt="profile" width={48} height={48} class="rounded-full" />

		<div class="flex-1 text-ellipsis">
			<h4 class="text-small-medium text-light-1">
				{`${firstName} ${lastName}`}
				{#if verified}
					<span class="pl-1 text-green-400 rounded-full float-right">
						<Icon icon="ic:round-verified" class="w-5 h-5" />
					</span>
				{/if}
			</h4>
			<p class="text-small-medium text-gray-1">@{firstName.toLowerCase()}</p>
			<div class="text-x-small-semibold p-1 text-light-1 bg-greenPrimary rounded">{speciality}</div>
		</div>
	</div>
	<div class="hidden lg:block">
		<p class="mt-2 text-subtle-medium text-gray-1">{bio}</p>
	</div>
	<div class="flex gap-3">
		<button class="button-icon" title="more details" on:click={() => goto('/care-givers')}>
			<Icon icon="mdi:show" height="20" />
		</button>
		<button class="button-icon" title="Sent email">
			<Icon icon="ic:baseline-email" height="20" />
		</button>
		<button class="button-icon" title="schedule appointment" on:click={() => goto('/care-givers')}>
			<Icon icon="ion:calendar" height="20" />
		</button>
		<button class="button-icon" title="start video call">
			<Icon icon="carbon:video-filled" height="20" />
		</button>
	</div>
</div>
