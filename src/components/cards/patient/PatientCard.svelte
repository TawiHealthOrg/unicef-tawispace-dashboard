<script>
	import Icon from '@iconify/svelte';
	import ProfileImage from '../../../lib/images/assets/images/profile1.jpg';
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
		<span class="button-icon">
			<Icon icon="mdi:show" height="20" />
		</span>
		<span class="button-icon">
			<Icon icon="ic:baseline-email" height="20" />
		</span>
		<span class="button-icon">
			<Icon icon="ion:calendar" height="20" />
		</span>
		<span class="button-icon">
			<Icon icon="carbon:video-filled" height="20" />
		</span>
	</div>
</article>
