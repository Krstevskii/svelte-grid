<script>
  import Grid from "./grid/Grid.svelte";
  import { data } from "./mock-data/mock-data.js";

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
</script>

<style>
  h1 {
    color: purple;
  }
</style>

<Grid gridData={data} {gridConfig} />
