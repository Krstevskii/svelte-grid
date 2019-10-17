<script>
  import { createEventDispatcher } from "svelte";

  // components
  import GridHeaderCell from "./GridHeaderCell.svelte";

  // input properties
  export let gridConfig = undefined;
  export let gridInitialSort = undefined;
  export let sort = undefined;

  const dispatch = createEventDispatcher();

  function handleChangeInSort(event) {
    const { sort: changedSort } = event.detail;

    if (sort.sortField === changedSort.sortField) {
      if (sort.sortOrder === "desc") {
        sort.sortOrder = "asc";
      } else {
        sort.sortOrder = "desc";
      }
    } else {
      sort = {
        ...changedSort
      };
    }

    dispatch("changeSort", {
      sort
    });
  }
</script>

<style>

</style>

<thead>
  <tr>
    {#each gridConfig as config, i}
      <GridHeaderCell {config} {sort} on:changeSort={handleChangeInSort} />
    {/each}
  </tr>
</thead>
