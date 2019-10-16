<script>
  //component
  import GridHeader from "./GridHeader.svelte";
  export let gridData = undefined;
  export let gridConfig = undefined;
</script>

<style>
  table {
    width: 100%;
  }
</style>

<table class="grid">
  <GridHeader {gridConfig} />
</table>
