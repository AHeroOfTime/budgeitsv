<script lang="ts">
	import MonthlyIncome from '../components/MonthlyIncome.svelte';
	import Spending from '../components/Spending.svelte';
	import Footer from '../components/Footer.svelte';

	let income = $state(50);
</script>

<div class="mx-auto grid max-w-4xl">
	<MonthlyIncome {income} />
	<div class="mb-5 grid gap-5 sm:grid-cols-1 md:grid-cols-2">
		<Spending spendingType={'Fixed'} />
		<Spending spendingType={'Variable'} />
	</div>
</div>

<Footer {income} />

<!-- TODO:
	-add reset button at top
	-logic for buttons, forms needed?
-->
