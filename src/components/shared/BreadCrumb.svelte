<script lang="ts">
	import Icon from "@iconify/svelte";
    export let baseLink:string;
    export let baseName: string;
    export let parentLink: string
    export let parentName: string
    export let childName: string
</script>
<nav class="flex p-3 text-gray-700 border border-gray-200 rounded-md bg-gray-50 dark:bg-gray-800 dark:border-gray-700" aria-label="Breadcrumb">
    <ol class="inline-flex items-center space-x-1 md:space-x-3">
      <li class="inline-flex items-center">
        <a href={baseLink} class="inline-flex items-center text-small-medium font-medium text-gray-700 hover:text-blue-600 dark:text-gray-400 dark:hover:text-white">
          <Icon icon="ic:baseline-home" aria-hidden="true" class="text-gray-400 w-5 h-5"/>
          {baseName}
        </a>
      </li>
      <li>
        <div class="flex items-center">
            <Icon icon="prime:angle-right" aria-hidden="true" class="text-gray-400 w-8 h-8"/>
          <a href={parentLink} class="ml-1 text-small-medium font-medium text-gray-700 hover:text-blue-600 dark:text-gray-400 dark:hover:text-white">{parentName}</a>
        </div>
      </li>
      <li aria-current="page">
        <div class="flex items-center">
            <Icon icon="prime:angle-right" aria-hidden="true" class="text-gray-400 w-8 h-8"/>
          <span class="ml-1 text-small-medium font-medium text-gray-500 dark:text-gray-400">{childName}</span>
        </div>
      </li>
    </ol>
</nav>