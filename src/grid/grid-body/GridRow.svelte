<script>
  import GridCell from "./GridCell.svelte";

  export let gridRowData = undefined;
  export let gridConfig = undefined;

  let rowDataToBeDisplayed = [];

  for (let [key, value] of Object.entries(gridRowData)) {
    rowDataToBeDisplayed.push([key, value]);
  }

  console.log("rowDataToBeDisplayed", rowDataToBeDisplayed);
</script>

<tr>
  {#each rowDataToBeDisplayed as cellData, i}
    <GridCell {cellData} />
  {/each}
</tr>
