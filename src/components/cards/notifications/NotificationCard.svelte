<script lang="ts">
	import Icon from '@iconify/svelte';
    export let ProfileImage:string,communityName:string,activityDescription:string,time:string
</script>
<article class="flex w-full flex-col rounded-xl bg-dark-2 p-7">
    <div class="flex items-start justify-between">
      <div class="flex w-full flex-1 flex-row gap-4">
        <div class="flex flex-col items-center">
          <a href="/"
            class="relative h-11 w-11">
            <img src={ProfileImage} alt="Profile"
              class="cursor-pointer rounded-full"
            />
          </a>
          <div class="thread-card_bar" />
        </div>
        <div class="flex w-full flex-col">
          <a href={`/profile/1`} class="">
            <h4 class="cursor-pointer text-base-semibold text-light-1">
              {communityName}
            </h4>
          </a>
          <p class="mt-2 text-small-regular text-light-2">
            {activityDescription}
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
            <p class="text-subtle-medium text-gray-1">Posted by,{communityName}</p>
            <p class="text-x-small-semibold inline-flex items-center gap-1 text-gray-1"><span><Icon icon="ri:time-line" /></span>{time}</p>
          </a>
        </div>
      </div>
    </div>
  </article>