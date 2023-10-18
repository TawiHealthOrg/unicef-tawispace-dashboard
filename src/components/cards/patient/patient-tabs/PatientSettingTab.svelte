<script>
	import Icon from "@iconify/svelte";

</script>
<section class="text-light-1 dashboard-card w-full">
    <h2>Account setting</h2>
    <div class="grid">
        <div class="inline-flex items-center gap-1 shadow-lg p-3">
            <Icon icon="codicon:account" class="w-5 h-5" /> <span>Account</span>
        </div>
        <div class="inline-flex items-center gap-1 shadow-lg p-3">
            <Icon icon="arcticons:password" class="w-5 h-5" /> <span>Password</span>
        </div>
        <div class="inline-flex items-center gap-1 shadow-lg p-3">
            <Icon icon="clarity:notification-solid" class="w-5 h-5" /> <span>Notification</span>
        </div>
        <div class="inline-flex items-center gap-1 shadow-lg p-3">
            <Icon icon="material-symbols:help" class="w-5 h-5"  /> <span>Help</span>
        </div>
    </div>
</section>