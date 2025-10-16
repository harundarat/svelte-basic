<script>
  import Todo from "./Todo.svelte";
</script>

<ul>
  <li>
    <Todo id="1" name="Belajar HTML" done={true} />
  </li>
  <li>
    <Todo id="2" name="Belajar CSS" done={false} />
  </li>
  <li>
    <Todo id="3" name="Belajar Javascript" done={false} />
  </li>
</ul>
