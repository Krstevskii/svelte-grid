<script>
  // components
  import GridRow from "./GridRow.svelte";

  export let gridConfig = undefined;
  export let gridData = undefined;
</script>

<tbody>
  {#each gridData as data, i}
    <GridRow gridRowData={data} {gridConfig} />
  {/each}
</tbody>
