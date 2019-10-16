<script>
  import Grid from "./grid/Grid.svelte";
  import { data } from "./mock-data/mock-data.js";

  const initialSort = {
    sortField: "id",
    sortOrder: "desc"
  };

  const gridConfig = [
    {
      headerLabel: "ID",
      headerField: "id",
      isSortable: true
    },
    {
      headerLabel: "Last name",
      headerField: "last_name",
      isSortable: true
    },
    {
      headerLabel: "Email",
      headerField: "email",
      isSortable: true
    },
    {
      headerLabel: "Gender",
      headerField: "gender",
      isSortable: true
    },
    {
      headerLabel: "Job",
      headerField: "job",
      isSortable: true
    }
  ];

  function handleChangeInSort(event) {
    const { sort } = event.detail;
    console.log(sort);
  }
</script>

<style>
  h1 {
    color: purple;
  }
</style>

<Grid
  gridInitialSort={initialSort}
  gridData={data}
  {gridConfig}
  on:changeSort={handleChangeInSort} />
