<script lang="ts">
	import Icon from '@iconify/svelte';
</script>
<article class="flex w-full flex-col rounded-xl bg-dark-2 p-7">
    <div class="flex items-start justify-between">
      <div class="flex w-full flex-1 flex-row gap-4">
        <div class="flex flex-col items-center">
          <a href="/"
            class="relative h-11 w-11">
            <img src={`https://source.boringavatars.com/pixel`} alt="Profile"
              class="cursor-pointer rounded-full"
            />
          </a>
          <div class="thread-card_bar" />
        </div>
        <div class="flex w-full flex-col">
          <a href={`/profile/1`} class="">
            <h4 class="cursor-pointer text-base-semibold text-light-1">
              KNH Community group
            </h4>
          </a>
          <p class="mt-2 text-small-regular text-light-4">
            Virginia Kring , joined the community
          </p>
          <div class="mt-5 flex flex-col gap-3">
            <div class="flex gap-3.5">
              <span class="text-light-2 cursor-pointer object-contain">
                <Icon icon="mdi:heart" height="24" />
              </span>
              <span class="text-light-2 cursor-pointer object-contain">
                <Icon icon="ic:baseline-reply" height="24" />
              </span>
              <span class="text-light-2 cursor-pointer object-contain">
                <Icon icon="quill:chat" height="24" />
              </span>
              <span class="text-light-2 cursor-pointer object-contain">
                <Icon icon="material-symbols:share" height="24" />
              </span>
            </div>
          </div>
          <a href="/communities/1" class="mt-5 items-center"> 
            <p class="text-x-small-semibold inline-flex items-center gap-1 text-gray-1"><span><Icon icon="ri:time-line" /></span>2 min ago</p>
          </a>
        </div>
      </div>
    </div>
    <div class="flex items-start justify-between">
      <div class="flex w-full flex-1 flex-row gap-4">
        <div class="flex flex-col items-center">
          <a href="/"
            class="relative h-11 w-11">
            <img src={`https://source.boringavatars.com/pixel`} alt="Profile"
              class="cursor-pointer rounded-full"
            />
          </a>
          <div class="thread-card_bar" />
        </div>
        <div class="flex w-full flex-col">
          <a href={`/profile/1`} class="">
            <h4 class="cursor-pointer text-base-semibold text-light-1">
              KNH Community group
            </h4>
          </a>
          <p class="mt-2 text-small-regular text-light-4">
            Admin posted announcement
          </p>
          <div class="mt-5 flex flex-col gap-3">
            <div class="flex gap-3.5">
              <span class="text-light-2 cursor-pointer object-contain">
                <Icon icon="mdi:heart" height="24" />
              </span>
              <span class="text-light-2 cursor-pointer object-contain">
                <Icon icon="ic:baseline-reply" height="24" />
              </span>
              <span class="text-light-2 cursor-pointer object-contain">
                <Icon icon="quill:chat" height="24" />
              </span>
              <span class="text-light-2 cursor-pointer object-contain">
                <Icon icon="material-symbols:share" height="24" />
              </span>
            </div>
          </div>
          <a href="/communities/1" class="mt-5 items-center"> 
            <p class="text-x-small-semibold inline-flex items-center gap-1 text-gray-1"><span><Icon icon="ri:time-line" /></span>15 min ago</p>
          </a>
        </div>
      </div>
    </div>
    <div class="flex items-start justify-between">
      <div class="flex w-full flex-1 flex-row gap-4">
        <div class="flex flex-col items-center">
          <a href="/"
            class="relative h-11 w-11">
            <img src={`https://source.boringavatars.com/pixel`} alt="Profile"
              class="cursor-pointer rounded-full"
            />
          </a>
          <div class="thread-card_bar" />
        </div>
        <div class="flex w-full flex-col">
          <a href={`/profile/1`} class="">
            <h4 class="cursor-pointer text-base-semibold text-light-1">
              KNH Community group
            </h4>
          </a>
          <p class="mt-2 text-small-regular text-light-4">
            Admin scheduled group virtual event
          </p>
          <div class="mt-5 flex flex-col gap-3">
            <div class="flex gap-3.5">
              <span class="text-light-2 cursor-pointer object-contain">
                <Icon icon="mdi:heart" height="24" />
              </span>
              <span class="text-light-2 cursor-pointer object-contain">
                <Icon icon="ic:baseline-reply" height="24" />
              </span>
              <span class="text-light-2 cursor-pointer object-contain">
                <Icon icon="quill:chat" height="24" />
              </span>
              <span class="text-light-2 cursor-pointer object-contain">
                <Icon icon="material-symbols:share" height="24" />
              </span>
            </div>
          </div>
          <a href="/communities/1" class="mt-5 items-center"> 
            <p class="text-x-small-semibold inline-flex items-center gap-1 text-gray-1"><span><Icon icon="ri:time-line" /></span>1hr ago</p>
          </a>
        </div>
      </div>
    </div>
  </article>