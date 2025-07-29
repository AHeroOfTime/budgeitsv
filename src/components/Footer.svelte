<script>
	let { income } = $props();
</script>

<footer class="bg-gray-800 p-4 text-white">
	<div class="mx-auto max-w-4xl">
		<ul>
			<li>
				Monthly Income:
				<span>${income}</span>
			</li>
			<li>
				Total Spending:
				<span>$VALUE</span>
			</li>
			<li>
				Disposable Income:
				<span>$VALUE</span>
			</li>
			<!-- Add section for savings? -->
		</ul>
	</div>
</footer>
