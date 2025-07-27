<script lang="ts">
	import MonthlyIncome from '../components/MonthlyIncome.svelte';
	import Spending from '../components/Spending.svelte';
</script>

<div class="mx-auto grid max-w-4xl">
	<MonthlyIncome />
	<div class="">
		<Spending spendingType={'Fixed'} />
		<Spending spendingType={'Variable'} />
	</div>
</div>
