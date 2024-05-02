<script>
	import Chart from 'chart.js/auto'
	export let config
	
	const handleChart = (element, config) => {
		let theChart = new Chart(element, config)
		
		return {
			update(config) {
				theChart.destroy()
				theChart = new Chart(element, config)
			},
			destroy() {
				theChart.destroy()
			}
		}
	}
</script>

<canvas use:handleChart={config} />