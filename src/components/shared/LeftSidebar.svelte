<script lang="ts">
import { HiSquares2X2 } from "react-icons/hi2";
import Icon from '@iconify/svelte';

let SidebarMenus = [
    {
    icon: "material-symbols:dashboard-customize",
    route: "/",
    label: "Dashboard",
  },
  {
    icon: "mdi:patient",
    route: "/patients",
    label: "Patients",
  },
  {
    icon: "fontisto:doctor",
    route: "/care-givers",
    label: "Caregivers",
  },
  {
    icon: "clarity:group-solid",
    route: "/communities",
    label: "Communities",
  },
  {
    icon: "basil:notification-solid",
    route: "/notifications",
    label: "Notifications",
  },
  {
    icon: "fa:user",
    route: "/profile",
    label: "Profile",
  },
]
</script>

<section class="custom-scrollbar leftsidebar">
    <div class="flex w-full flex-1 flex-col gap-6 px-6">
        {#each SidebarMenus as menu}
            <a href={menu.route} class="leftsidebar_link bg-gradient-to-tr from-greenPrimary to-primary">
                <span class="text-white"><Icon icon={menu.icon} height={24} /></span>
                <p class="text-light-1 max-lg:hidden">{menu.label}</p>
            </a>
        {/each}
    </div>
    <!-- logout at the bottom -->
            <div class="mt-10 px-6">
                <div class="flex cursor-pointer gap-4 p-4">
                    <span class="text-white " >
                      <Icon icon="heroicons-outline:logout" height={24} />
                    </span>
                    <p class="text-light-2 max-lg:hidden">Logout</p>
                </div>
            </div>
</section>
