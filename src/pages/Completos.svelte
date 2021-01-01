<script>
  import { onMount } from "svelte";
  import Item from "../components/Item.svelte";
  import Back from "../components/Back.svelte";
  import drive from "drive-db";
  let db = [];
  onMount(async () => {
    db = await drive("1w7DdwTiFllZ4Mg4nVWNFF6g2TKnGjsICo9ioFJwcXDw");
    db.reverse();
  });
</script>

<Back />
{#each db as item}
  <Item {item} />
{/each}
