<script lang="ts">
	import Icon from '@iconify/svelte';
	import ProfileImage from '../../../lib/images/assets/images/profile1.jpg';
	import { Communities } from '../../../data/SomeData'
</script>

{#each Communities as community}
	<section class="community-card">
		<div class="flex flex-wrap items-center gap-3">
			<a href={`/communities/1`} class="relative h-12 w-12">
				<img src={community.photoURL} alt={community.name} class="rounded-full object-cover" />
			</a>
			<div>
				<a href={`/communities/1`} class="inline-flex items-center">
					<h4 class="text-base-semibold text-light-1">{community.name}</h4> 
          {#if community.verified}
            <span class="pl-1 text-gold rounded-full float-right">
              <Icon icon="ic:round-verified" class="w-5 h-5" />
            </span>
          {/if}
				</a>
				<p class="text-small-medium text-gray-1">@{community.username}</p>
			</div>
		</div>
		<p class="mt-4 text-subtle-medium text-gray-1">{community.description}</p>
		<div class="mt-5 flex flex-wrap items-center justify-start gap-3">
			<span class="button-icon">
				<Icon icon="mdi:show" height="20" />
			</span>
			<span class="button-icon">
				<Icon icon="material-symbols:share" height="20" />
			</span>
		</div>
	</section>
{/each}
