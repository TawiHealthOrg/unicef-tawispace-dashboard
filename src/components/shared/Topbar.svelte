<script lang="ts">
    import Logo from "../../lib/images/assets/logos/tawiHealthLogo-transparent.png"
</script>

<nav class="topbar">
    <a href="/" class="flex items-center gap-4">
        <picture>
            <img src={Logo} alt="tawihealth logo" width={28} height={28} />
        </picture>

        <p class="text-heading3-bold text-light-1 max-xl:hidden">Tawispace</p>
    </a>
    <div class="flex item-center gap-1">
        <div class="block md:hidden">
            <div class="flex cursor-pointer text-light-1">
                Logout
            </div>
        </div>
    </div>
</nav>
