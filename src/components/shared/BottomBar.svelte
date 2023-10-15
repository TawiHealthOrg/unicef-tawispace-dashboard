<script lang="ts">
	import Icon from "@iconify/svelte";
	import { space } from "postcss/lib/list";
  import {page} from '$app/stores'
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
    label: "Communities and",
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

$: currentPage = $page.url.pathname
</script>

<section class="bottombar">
    <div class="bottombar_container">
      {#each SidebarMenus as menu}
         <a
            href={menu.route}
            class={`${currentPage === menu.route ? 'bottombar_link bg-gradient-to-tr from-greenPrimary to-primary' :'bottombar_link' }`}>
            <span class="text-white"><Icon icon={menu.icon} height={24} /></span>
            <p class="text-subtle-medium text-light-1 max-sm:hidden">
              {menu.label.split(/\s+./)[0]}
            </p>
          </a>
      {/each
       
        }
    </div>
  </section>