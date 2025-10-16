<script>
  import EditTodo from "./EditTodo.svelte";
  import Todo from "./Todo.svelte";

  let data = $state([]);

  let id = 0;

  const add = (e) => {
    e.preventDefault();

    const input = document.getElementById("todo");
    data.push({
      id: id++,
      name: input.value,
    });
    input.value = "";
  };

  const remove = (id) => {
    data = data.filter((todo) => todo.id !== id);
  };

  const edit = (id) => {
    for (let i = 0; i < data.length; i++) {
      if (data[i].id === id) {
        data[i] = { ...data[i], edit: true };
      }
    }
  };

  const onEdit = (id, name) => {
    for (let i = 0; i < data.length; i++) {
      if (data[i].id === id) {
        data[i] = { id, name, edit: false };
      }
    }
  };
</script>

<form>
  <input type="text" id="todo" />
  <button onclick={add}>Add</button>
</form>

<ul>
  {#each data as todo (todo.id)}
    <li>
      {#if todo.edit}
        <EditTodo id={todo.id} name={todo.name} onedit={onEdit} />
      {:else}
        <Todo {...todo} />
        <button onclick={() => edit(todo.id)}>Edit</button>
        <button onclick={() => remove(todo.id)}>Remove</button>
      {/if}
    </li>
  {/each}
</ul>
