<script>
	import Node from '$lib/Node.svelte';

	let STARTING_NODE_ROW = 10;
	let STARTING_NODE_IDX = 4;
	let ENDING_NODE_ROW = 10;
	let ENDING_NODE_IDX = 45;

	let nodes = [];

	// TODO: make this responsive based on screen size
	for (let row = 0; row < 20; row++) {
		const currentRow = [];
		for (let col = 0; col < 50; col++) {
			let node = {
				row,
				col,
				isStart: row == STARTING_NODE_ROW && col == STARTING_NODE_IDX,
				isEnd: row == ENDING_NODE_ROW && col == ENDING_NODE_IDX,
			};
			currentRow.push(node);
		}
		nodes.push(currentRow);
	}
</script>

<div class="grid">
	{#each nodes as row}
		<div class="row">
			{#each row as node}
				<Node {...node} />
			{/each}
		</div>
	{/each}
</div>

<style>
	.grid {
		margin: 100px 0 0;
	}
</style>
