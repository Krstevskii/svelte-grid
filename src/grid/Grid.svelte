<script>
  //component
  import GridHeader from "./grid-header/GridHeader.svelte";
  import GridBody from "./grid-body/GridBody.svelte";

  // input properties
  export let gridData = undefined;
  export let gridConfig = undefined;
  export let gridInitialSort = undefined;

  let sort = {
    ...gridInitialSort
  };
</script>

<style>
  table {
    width: 100%;
  }
</style>

<table class="grid">
  <GridHeader {sort} {gridConfig} {gridInitialSort} on:changeSort />
  <GridBody {gridConfig} {gridData} />
</table>
