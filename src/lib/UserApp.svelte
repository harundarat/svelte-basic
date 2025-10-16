<script>
  import UserRow from "./UserRow.svelte";

  const user = {
    id: 1,
    name: "Harun",
    address: "Indonesia",
  };
</script>

<table>
  <thead>
    <tr>
      <th>ID</th>
      <th>Name</th>
      <th>Address</th>
    </tr>
  </thead>
  <tbody>
    <UserRow {...user} />
  </tbody>
</table>
