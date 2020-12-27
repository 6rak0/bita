<script>
	import drive from "drive-db";
	import { onMount } from "svelte";
	import Item from "./Item.svelte";

	let db = [];

	onMount(async () => {
		db = await drive("1w7DdwTiFllZ4Mg4nVWNFF6g2TKnGjsICo9ioFJwcXDw");
		db.reverse();
	});
</script>

<div class="m-3">
	<h1 class="text-center">
		<i class="fas fa-virus text-green-700" />
		evolución
		<i class="fas fa-virus text-green-700" />
	</h1>
</div>

{#each db as item}
	<Item {item} />
{/each}
