<script>
  //component
  import GridHeader from "./GridHeader.svelte";
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
</table>
