<script>
  import { counter } from "../state/counter.svelte";

  const increment = () => {
    counter.count++;
  };
</script>

<button onclick={increment}>Increment: {counter.count}</button>
