<script lang="ts">
	import Icon from '@iconify/svelte';
    import ProfileImage from '../../../lib/images/assets/images/profile1.jpg'
</script>

<section class="community-card">
    <div class="flex flex-wrap items-center gap-3">
      <a href={`/communities/1`} class="relative h-12 w-12">
        <img
          src={ProfileImage}
          alt="community_logo"
          
          class="rounded-full object-cover"
        />
      </a>
      <div>
        <a href={`/communities/1`}>
          <h4 class="text-base-semibold text-light-1">{`KNH Community Group`}</h4>
        </a>
        <p class="text-small-medium text-gray-1">@{`knhcomms`}</p>
      </div>
    </div>
    <p class="mt-4 text-subtle-medium text-gray-1">{`Community group for KNH for Nairobi HIV`}</p>
    <div class="mt-5 flex flex-wrap items-center justify-start gap-3">
      <span class="button-icon" >
        <Icon icon="mdi:show" height="20"/>
      </span>
      <span class="button-icon">
        <Icon icon="material-symbols:share" height="20"/>
      </span>
    </div>
  </section>