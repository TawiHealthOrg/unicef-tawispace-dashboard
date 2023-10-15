<script>
	import Icon from '@iconify/svelte';
	import ProfileImage from '../../../lib/images/assets/images/profile1.jpg';
	import { goto } from '$app/navigation';
</script>

<article class="user-card">
	<div class="user-card_avatar">
		<img src={ProfileImage} alt="ii" width={48} height={48} class="rounded-full" />
		<div class="flex-1 text-ellipsis">
			<h4 class="text-base-semibold text-light-1">John Doe</h4>
			<p class="text-small-medium text-gray-1">@johndoe</p>
		</div>
	</div>
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
