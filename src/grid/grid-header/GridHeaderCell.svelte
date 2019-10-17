<script>
  import { createEventDispatcher } from "svelte";

  // input properties
  export let config = undefined;
  export let sort = undefined;
  const dispatch = createEventDispatcher();

  function changeSort() {
    dispatch("changeSort", {
      sort: {
        sortField: config.headerField,
        sortOrder: "desc"
      }
    });
  }
</script>

<style>
  th {
    text-align: left;
  }

  .singleHeaderCell > div {
    display: inline-block;
  }

  .sort {
    cursor: pointer;
  }
</style>

<th>
  <div class="singleHeaderCell">
    <div class="headerLabel">
      <p>{config.headerLabel}</p>
    </div>
    {#if config.isSortable}
      <div class="sort" on:click={changeSort}>
        <div
          class="carret-up"
          style="border-bottom: 6px solid {sort.sortField === config.headerField && sort.sortOrder === 'asc' ? '#385E98' : 'black'}" />
        <div
          class="carret-down"
          style="border-top: 6px solid {sort.sortField === config.headerField && sort.sortOrder === 'desc' ? '#385E98' : 'black'}" />
      </div>
    {/if}
  </div>
</th>
