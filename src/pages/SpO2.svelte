<script>
  import Back from "../components/Back.svelte";
  import { onMount } from "svelte";
  import drive from "drive-db";
  let db = [];
  onMount(async () => {
    db = await drive("126HofkrcA65tasl3do4-F-8KRMDQ0ZN8G4anFnNyq48");
    db.reverse();
  });
</script>

<div class="m-3 text-center">
  <h1 class="m-3">SpO²</h1>
  {#each db as item}
    <div class="flex justify-around">
      <div>{item.tiempo}</div>
      <div>{item.oxigenación}%</div>
    </div>
  {/each}
</div>

<Back />
