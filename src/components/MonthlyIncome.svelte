<script>
	let income = $state(0);
</script>

<div class="mt-5 px-3 py-5 shadow">
	<h3 class="mb-3">Monthly Income</h3>
	<div class="grid grid-cols-2 gap-2">
		<div
			class="grid grid-cols-[auto_1fr] items-center overflow-hidden rounded-lg border border-gray-300"
		>
			<span class="bg-gray-100 px-4 py-2">$</span>
			<input class="w-full p-2 focus:outline-none" type="number" bind:value={income} />
		</div>
		<button class="mt-1 grid-cols-1 rounded-lg bg-green-600 p-2 text-white hover:bg-green-700"
			>Submit</button
		>
	</div>
</div>
