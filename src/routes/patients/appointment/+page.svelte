<script lang="ts">
	import BreadCrumb from '../../../components/shared/BreadCrumb.svelte';
</script>

<section class="">
	<div>
		<BreadCrumb
			baseLink="/"
			baseName="Tawispace"
			parentLink="/patients"
			parentName="Patient"
			childName="re-schedule Appointment"
		/>
		<div class="py-4 hidden md:block">
			<p class="text-small-medium text-gray-1">Re-schedule appointment with patients.</p>
		</div>
	</div>
	<div class="form-card">
		<form autoComplete="off" class="text-small-regular">
			<div class="grid sm:grid-cols-2 gap-4">
				<div class="mb-4">
					<label for="email" class="block mb-2 text-sm font-medium text-light-1">
						Patient name
					</label>
					<select
						class=" text-gray-900 text-sm rounded-lg block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white"
						placeholder="select patient"
					>
						<option>--Select Patient--</option>
					</select>
				</div>
				<div class="mb-4">
					<label for="email" class="block mb-2 font-medium text-light-1"> Email </label>
					<input
						type="email"
						id="email"
						class="border rounded-lg focus:ring-gray-1 focus:border-gray-1 block w-full p-2.5 bg-gray-700 border-gray-600 placeholder-gray-400 text-white"
						placeholder="Enter email"
					/>
				</div>
			</div>
			<div class="grid sm:grid-cols-2 gap-4">
				<div class="mb-4">
					<label for="startdate" class="block mb-2 font-medium text-light-1"> From: </label>
					<input
						type="datetime-local"
						class="border text-sm rounded-lg focus:ring-gray-700 focus:border-gray-700 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 text-white"
					/>
				</div>
				<div class="mb-4">
					<label for="email" class="block mb-2 text-sm font-medium text-light-1"> To: </label>
					<input
						type="datetime-local"
						id="email"
						class="border text-sm rounded-lg focus:ring-gray-700 focus:border-gray-700 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 text-white"
						placeholder="enter email"
					/>
				</div>
			</div>
			<div class="grid grid-cols-1 mb-4">
				<label for="notes" class="block mb-2 text-sm font-medium text-light-1"> Notes </label>
				<textarea
					class="bg-gray-700 text-gray-100 border rounded-md dark:border-gray-600 p-2"
					cols="30"
					rows="10"
				/>
			</div>
			<button type="submit" class="form-btn">Submit</button>
		</form>
	</div>
</section>
