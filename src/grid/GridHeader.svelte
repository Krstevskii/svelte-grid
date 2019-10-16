<script>
  export let gridConfig = undefined;
</script>

<style>
  th {
    text-align: left;
  }
</style>

<thead>
  <tr>
    {#each gridConfig as config, i}
      <th>{config.headerLabel}</th>
    {/each}
  </tr>
</thead>
