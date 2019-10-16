<script>
  import Grid from "./grid/Grid.svelte";
  import { data } from "./mock-data/mock-data.js";

  const gridConfig = [
    {
      headerLabel: "ID",
      headerField: "id"
    },
    {
      headerLabel: "Last name",
      headerField: "last_name"
    },
    {
      headerLabel: "Email",
      headerField: "email"
    },
    {
      headerLabel: "Gender",
      headerField: "gender"
    },
    {
      headerLabel: "Job",
      headerField: "job"
    }
  ];
</script>

<style>
  h1 {
    color: purple;
  }
</style>

<Grid gridData={data} {gridConfig} />
