<script lang="ts">
	import NotificationCard from '../../components/cards/notifications/NotificationCard.svelte';
</script>

<h3 class="text-heading4-medium text-light-1">Notifications</h3>
<section class="mt-9 flex flex-col gap-10">
	<NotificationCard
		communityName="KNH Community group"
		ProfileImage={`https://source.boringavatars.com/pixel`}
        activityDescription="Virginia joined the community"
        time="5mins ago"
	/>
	<NotificationCard
		communityName="KNH Community group"
		ProfileImage="https://source.boringavatars.com/pixel"
        activityDescription="Admin made an announcement."
        time="43 min ago"
	/>
	<NotificationCard
		communityName="Allcare Community group"
		ProfileImage={`https://source.boringavatars.com/beam`}
        activityDescription="Adler joined the community."
        time="1hr ago"
	/>
	<NotificationCard
		communityName="Lifeline group"
		ProfileImage={`https://source.boringavatars.com/ring`}
        activityDescription="Adler joined the community."
        time="2hr ago"
	/>
	<NotificationCard
		communityName="HealthDose community"
		ProfileImage={`https://source.boringavatars.com/`}
        activityDescription="Adler joined the community."
        time="1 days ago"
	/>
	<NotificationCard
		communityName="KNH Community group"
		ProfileImage={`https://source.boringavatars.com/bauhaus`}
        activityDescription="Adler joined the community."
        time="2 days ago"
	/>
</section>
