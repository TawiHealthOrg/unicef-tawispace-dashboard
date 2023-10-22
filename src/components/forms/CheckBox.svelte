<script lang="ts">
export let yes=false
</script>

<div class="flex items-center">
	<input
		id="link-checkbox"
		type="checkbox"
		bind:checked={yes}
		class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 rounded focus:ring-primary dark:focus:ring-primary dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600"
	/>
	<label for="link-checkbox" class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300"
		>I agree with the <a
			href="https://tawihealth.com/privacy/our-terms-of-use"
			target="_blank"
			class="text-primary dark:text-blue-500 hover:underline">terms and conditions</a
		>.</label
	>
</div>
