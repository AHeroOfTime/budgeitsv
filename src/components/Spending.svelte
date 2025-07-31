<script lang="ts">
	import { derived } from 'svelte/store';

	let { spendingType } = $props();
	let totalAmount = $derived(0);
	let expenses = $state([
		{
			title: '',
			cost: 0
		}
	]);

	const addExpense = () => {
		console.log(expenses[0].cost);
	};
</script>

<div class="mt-5 rounded-md border border-gray-300 shadow">
	<h3 class="mb-5 border-b-1 border-gray-200 bg-gray-100 px-3 py-3 font-semibold">
		{spendingType} Spending
	</h3>
	<div class="grid grid-cols-2 gap-2 px-3 pb-5">
		<!-- Item label + input -->
		<div class="flex flex-col">
			<label class="mb-1 text-sm font-bold text-gray-700" for="item">Expense</label>
			<input
				id="expense"
				class="w-full rounded-lg border border-gray-300 p-2 shadow-sm focus:ring-2 focus:ring-green-600 focus:outline-none invalid:focus:ring-red-500"
				type="text"
				placeholder="Add expense"
			/>
		</div>

		<!-- Amount input with $ prefix -->
		<div class="flex flex-col">
			<label class="mb-1 text-sm font-bold text-gray-700" for="amount">Amount</label>
			<div class="flex items-center rounded-lg border border-gray-300">
				<span class="border-r border-gray-200 bg-gray-100 px-4 py-2">$</span>
				<input
					id="amount"
					class="w-full rounded-r-lg border-0 p-2 focus:ring-2 focus:ring-green-600 focus:outline-none invalid:focus:ring-red-500"
					type="number"
					placeholder="Amount"
				/>
			</div>
		</div>

		<button
			onclick={() => addExpense()}
			class="col-span-2 mt-2 rounded-lg bg-green-600 p-2 text-white hover:bg-green-700"
			>Submit</button
		>

		<!-- Expense List -->
		<ul>
			<!-- {#each expenses as expense}
				<li>
					<strong>{expense.title}</strong>
					${expense.cost}
				</li>
			{/each} -->
		</ul>
		<div>
			Total {spendingType} Spending: ${totalAmount}
		</div>
	</div>
</div>
