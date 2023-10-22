<script lang="ts">
	import CheckBox from '../../../components/forms/CheckBox.svelte';
	import BreadCrumb from '../../../components/shared/BreadCrumb.svelte';
	let firstName: string,
		lastName: string,
		email: string,
		phone: string,
		gender: string,
		county: string,
		bio: string;

    let yes:boolean=true
</script>

<section class="">
	<!-- Breadcrumb -->
	<div class="hidden sm:block">
		<BreadCrumb
			baseLink="/"
			baseName="Tawispace"
			parentLink="/patients"
			parentName="Patients"
			childName="add patient"
		/>
	</div>

	<div class="form-card">
		<form autoComplete="off" class="text-small-regular">
			<div class="grid sm:grid-cols-2 gap-4">
				<div class="mb-4">
					<label for="firstname" class="block mb-2 text-sm font-medium text-light-1">
						First Name:
					</label>
					<input
						type="text"
						id="firstname"
						class="border rounded-lg focus:ring-gray-1 focus:border-gray-1 block w-full p-2.5 bg-gray-700 border-gray-600 placeholder-gray-400 text-white"
						placeholder="First name"
						bind:value={firstName}
					/>
				</div>
				<div class="mb-4">
					<label for="firstname" class="block mb-2 text-sm font-medium text-light-1">
						Last Name:
					</label>
					<input
						type="text"
						id="firstname"
						class="border rounded-lg focus:ring-gray-1 focus:border-gray-1 block w-full p-2.5 bg-gray-700 border-gray-600 placeholder-gray-400 text-white"
						placeholder="Last name"
						bind:value={lastName}
					/>
				</div>
			</div>
			<div class="grid sm:grid-cols-2 gap-4">
				<div class="mb-4">
					<label for="email" class="block mb-2 text-sm font-medium text-light-1"> Email: </label>
					<input
						type="email"
						id="email"
						class="border rounded-lg focus:ring-gray-1 focus:border-gray-1 block w-full p-2.5 bg-gray-700 border-gray-600 placeholder-gray-400 text-white"
						placeholder="Email address"
						bind:value={email}
					/>
				</div>
				<div class="mb-4">
					<label for="firstname" class="block mb-2 text-sm font-medium text-light-1">
						Phone number:
					</label>
					<input
						type="tel"
						id="firstname"
						class="border rounded-lg focus:ring-gray-1 focus:border-gray-1 block w-full p-2.5 bg-gray-700 border-gray-600 placeholder-gray-400 text-white"
						placeholder="Enter phone"
						bind:value={phone}
					/>
				</div>
			</div>
			<div class="grid sm:grid-cols-2 gap-4">
				<div class="mb-4">
					<label for="gender" class="block mb-2 font-medium text-light-1"> Gender: </label>
					<select
						class=" text-gray-900 text-sm rounded-lg block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white"
						placeholder="select patient"
						bind:value={gender}
					>
						<option value="">--Select Gender--</option>
						<option>Male</option>
						<option>Female</option>
						<option>Prefer not to say</option>
					</select>
				</div>
				<div class="mb-4">
					<label for="email" class="block mb-2 text-sm font-medium text-light-1"> Location: </label>
					<select
						class=" text-gray-900 text-sm rounded-lg block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white"
						placeholder="select patient"
						bind:value={county}
					>
						<option value="">--Select County--</option>
						<option>Nairobi</option>
						<option>Nakuru</option>
						<option>Mombasa</option>
						<option>Kisumu</option>
						<option>Kakamega</option>
					</select>
				</div>
			</div>
			<div class="grid grid-cols-1 mb-4">
				<label for="notes" class="block mb-2 text-sm font-medium text-light-1">Patient Bio: </label>
				<textarea
					class="bg-gray-700 text-gray-100 border rounded-md dark:border-gray-600 p-2"
					cols="30"
					rows="10"
					bind:value={bio}
				/>
			</div>
			<div class="mb-4">
				<CheckBox yes={true} />
			</div>
			<button disabled={!yes} type="submit" class="form-btn">submit</button>
		</form>
	</div>
</section>
