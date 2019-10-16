<script>
  import { createEventDispatcher } from "svelte";

  export let config = undefined;
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
</style>

<th>
  <div class="singleHeaderCell">
    <div class="headerLabel">
      <p>{config.headerLabel}</p>
    </div>
    {#if config.isSortable}
      <div class="sort" on:click={changeSort}>
        <div class="carret-up" />
        <div class="carret-down" />
      </div>
    {/if}
  </div>
</th>
