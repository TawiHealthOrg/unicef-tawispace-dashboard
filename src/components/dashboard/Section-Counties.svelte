<script lang="ts">
	import { onMount } from 'svelte';
	import Chart from 'chart.js/auto';
	let counties: any;
	const data = {
		labels: ['Kisumu', 'Nairobi', 'Lamu', 'Siaya', 'Kakamega'],
		datasets: [
			{
				label: 'Most prevalent areas',
				data: [300, 50, 10, 100, 200],
				backgroundColor: ['#7000e1', '#fc8800', '#358747', '#00b0e8', '#FFD700'],
				hoverOffset: 4,
				borderWidth: 0,
				fill: false,
				borderColor: 'rgb(75, 192, 192)',
				tension: 0.1
			}
		]
	};
	const config = {
		type: 'bar',
		data: data,
		options: {
			borderRadius: '20',
			responsive: true,
			cutout: '95%',
			spacing: 2,
			plugins: {
				legend: {
					position: 'bottom',
					display: true,
					labels: {
						usePointStyle: true,
						padding: 20,
						font: {
							size: 14
						}
					}
				},
				title: {
					display: true,
					text: 'Prevalent Counties in Kenya'
				}
			}
		}
	};
	onMount(() => {
		const ctx = counties.getContext('2d');
		// Initialize chart using default config set
		var myChart = new Chart(ctx, config);
	});
</script>

<section class="mt-9 grid grid-col-1 w-full">
	<div class="w-full rounded-lg bg-dark-3 px-4 py-5 h-full">
		<div class="flex flex-wrap items-center gap-3">
			<canvas bind:this={counties} class="w-full" />
		</div>
	
		<div class="mt-5 flex flex-wrap items-center justify-between gap-3" />
	</div>
</section>