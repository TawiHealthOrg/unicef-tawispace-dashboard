
<script lang="ts">
	import Icon from "@iconify/svelte";
  export let inputPlaceholder: string
</script>

<div class='searchbar'>
    <span class="text-light-1 inline-flex items-center"><Icon icon="iconamoon:search-light" height="24" /></span>
    <input
      class='no-focus searchbar_input w-full placeholder:text-small-medium'
      placeholder={inputPlaceholder}
    />
</div>