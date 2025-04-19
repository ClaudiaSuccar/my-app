<script lang="ts">
	let a = 0;
	let b = 0;
	let total = 0;

	async function add() {
		const response = await fetch('/api/add', {
			method: 'POST',
			body: JSON.stringify({ a, b }),
			headers: {
				'content-type': 'application/json'
			}
		});

		total = await response.json();
	}
</script>

<div class="grid" style="display: grid; grid-template-columns: 2fr .1fr 2fr 4fr;">
    <input type="number" bind:value={a}>+
    <input type="number" bind:value={b}>=
    {total}
</div>

<button onclick={add}>Calculate</button>