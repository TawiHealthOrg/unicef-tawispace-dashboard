<script lang="ts">
	import Icon from "@iconify/svelte";
import CommunityCard from "../../components/cards/community/CommunityCard.svelte";
	import SearchCommunity from "../../components/cards/community/SearchCommunity.svelte";


</script>

<div class="flex justify-between">
    <h1 class='text-heading4-medium text-light-1'>Communities</h1>
    <button title="Add community" class="button-icon inline-flex items-center gap-1 text-small-regular bg-gradient-to-tr from-greenPrimary to-primary max-sm:hidden"><Icon icon="icon-park-solid:add" /> community</button>
    <button title="Add community" class="button-icon text-small-regular bg-gradient-to-tr from-greenPrimary to-primary sm:hidden"><Icon icon="material-symbols:add" height="24" /></button>
</div>
<div class='mt-5'>
    <SearchCommunity  />
</div>
<section class='mt-5 grid sm:grid-cols-2 flex-wrap gap-5'>
    <CommunityCard />
</section>