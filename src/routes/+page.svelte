<script lang="ts">
	import MonthlyIncome from '../components/MonthlyIncome.svelte';
	import Spending from '../components/Spending.svelte';

	// let income = $state();
	let monthlyIncome = $state(0);
	let totalSpending = $state(0);
	let disposableIncome = $state(0);

	function updateIncome(newIncome: number) {
		monthlyIncome = newIncome;
	}
</script>

<div class="mx-auto grid max-w-4xl">
	<MonthlyIncome onUpdate={updateIncome} />
	<div class="mb-5 grid gap-5 sm:grid-cols-1 md:grid-cols-2">
		<Spending spendingType={'Fixed'} />
		<Spending spendingType={'Variable'} />
	</div>
</div>

<footer class="bg-gray-800 p-4 text-white">
	<div class="mx-auto max-w-4xl">
		<ul>
			<li>
				Monthly Income:
				<span>${monthlyIncome}</span>
			</li>
			<li>
				Total Spending:
				<span>${totalSpending}</span>
			</li>
			<li>
				Disposable Income:
				<span>${disposableIncome}</span>
			</li>
			<!-- Add section for savings? -->
		</ul>
	</div>
</footer>

<!-- TODO:
	-persist with local storage
	-add reset button at top
	-logic for buttons, forms needed?
-->
