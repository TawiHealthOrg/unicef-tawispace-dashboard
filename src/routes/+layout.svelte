<script>
	import RightSidebar from '../components/shared/RightSidebar.svelte';
	import Topbar from '../components/shared/Topbar.svelte';
	import BottomBar from '../components/shared/BottomBar.svelte'
	import LeftSidebar from '../components/shared/LeftSidebar.svelte'
	import './styles.css';
</script>

<div class="app">
	<Topbar />
    <main class="flex flex-row">
        <LeftSidebar />
        <section class="main-container ">
            <div class="w-full max-w-4xl"><slot /></div>
        </section>
        <RightSidebar />
    </main>
    <BottomBar />
</div>
