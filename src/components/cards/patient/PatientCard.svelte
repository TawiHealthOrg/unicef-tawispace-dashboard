<script lang="ts">
	import Icon from '@iconify/svelte';
	import { goto } from '$app/navigation';
	export let firstName:string,lastName:string,photoURL:string
</script>


	<article class="user-card">
		<a href="/patients/1" class=" hover:cursor-pointer">
			<div class="user-card_avatar">
				<img src={photoURL} alt={firstName} class="rounded-full w-10 h-10" />
				<div class="flex-1 text-ellipsis">
					<h4 class="text-small-medium text-light-1">{`${firstName} ${lastName}`}</h4>
					<p class="text-small-regular text-gray-1">@{lastName.toLowerCase()}</p>
				</div>
			</div>
		</a>
		<div class="flex gap-3.5">
			<button class="button-icon" on:click={() =>goto('/patients/1')}>
				<Icon icon="mdi:show" height="20" />
			</button>
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
	</article>


