<script>
  import Todo from "./Todo.svelte";

  const data = $state([
    {
      id: "1",
      name: "Belajar HTML",
      done: true,
    },
    {
      id: "2",
      name: "Belajar CSS",
      done: false,
    },
    {
      id: "3",
      name: "Belajar Javascript",
      done: true,
    },
    {
      id: "4",
      name: "Belajar Svelte",
      done: false,
    },
  ]);

  const remove = () => {
    data.shift();
  };
</script>

<button onclick={remove}>Remove</button>

<ul>
  {#each data as todo (todo.id)}
    <li>
      <Todo {...todo} />
    </li>
  {/each}
</ul>
