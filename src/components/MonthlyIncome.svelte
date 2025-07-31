<script>
	let { onUpdate } = $props();
	let incomeValue = $state();

	const updateIncome = () => {
		onUpdate(incomeValue);
		// clear input
		incomeValue = '';
	};
</script>

<div class="mt-5 rounded-md border border-gray-300 shadow">
	<h3 class="mb-5 border-b-1 border-gray-200 bg-gray-100 px-3 py-3 font-semibold">
		Monthly Income
	</h3>
	<div class="grid grid-cols-2 gap-2 px-3 pb-5">
		<div class="flex items-center rounded-lg border border-gray-300">
			<span class="border-r-1 border-gray-200 bg-gray-100 px-4 py-2">$</span>
			<input
				class="focus:ring-opacity-100 w-full rounded-r-lg border-0 p-2 focus:ring-2 focus:ring-green-600 focus:outline-none invalid:focus:ring-red-500"
				type="number"
				placeholder="Monthly Income"
				bind:value={incomeValue}
			/>
		</div>
		<button
			onclick={updateIncome}
			class="grid-cols-1 rounded-lg bg-green-600 p-2 text-white hover:bg-green-700">Submit</button
		>
	</div>
</div>
