<script lang="ts">
	import CheckBox from "../../../components/forms/CheckBox.svelte";
import BreadCrumb from "../../../components/shared/BreadCrumb.svelte";
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
                />
            </div>
        </div>
        <div class="grid sm:grid-cols-2 gap-4">
            <div class="mb-4">
                <label for="email" class="block mb-2 text-sm font-medium text-light-1">
                    Email:
                </label>
                <input
                    type="email"
                    id="email"
                    class="border rounded-lg focus:ring-gray-1 focus:border-gray-1 block w-full p-2.5 bg-gray-700 border-gray-600 placeholder-gray-400 text-white"
                    placeholder="Email address"
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
                />
            </div>
        </div>
        <div class="grid sm:grid-cols-2 gap-4">
            <div class="mb-4">
                <label for="gender" class="block mb-2 font-medium text-light-1"> Gender: </label>
                <select
						class=" text-gray-900 text-sm rounded-lg block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white"
						placeholder="select patient"
					>
						<option value="">--Select Gender--</option>
                        <option >Male</option>
                        <option >Female</option>
				</select>
            </div>
            <div class="mb-4">
                <label for="email" class="block mb-2 text-sm font-medium text-light-1"> Location: </label>
                <select
						class=" text-gray-900 text-sm rounded-lg block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white"
						placeholder="select patient"
					>
						<option value="">--Select County--</option>
                        <option >Nairobi</option>
                        <option >Nakuru</option>
                        <option >Mombasa</option>
                        <option >Kisumu</option>
                        <option >Kakamega</option>
				</select>
            </div>
        </div>
        <div class="grid grid-cols-1 mb-4">
            <label for="notes" class="block mb-2 text-sm font-medium text-light-1">Patient Bio: </label>
            <textarea
                class="bg-gray-700 text-gray-100 border rounded-md dark:border-gray-600 p-2"
                cols="30"
                rows="10"
            />
        </div>
        <div class="mb-4">
            <CheckBox />
        </div>
        <button type="submit" class="form-btn">submit</button>
    </form>
</div>

</section>