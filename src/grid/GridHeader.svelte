<script>
  export let gridConfig = undefined;
</script>

<style>
  th {
    text-align: left;
  }

  .singleHeaderCell > div {
    display: inline-block;
  }
</style>

<thead>
  <tr>
    {#each gridConfig as config, i}
      <th>
        <div class="singleHeaderCell">
          <div class="headerLabel">
            <p>{config.headerLabel}</p>
          </div>
          <div class="sort">
            <div class="carret-up" />
            <div class="carret-down" />
          </div>
        </div>
      </th>
    {/each}
  </tr>
</thead>
