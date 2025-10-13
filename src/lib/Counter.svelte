<script>
  let count = $state(0);

  const increment = () => count++;
</script>

<h1>Count: {count}</h1>

<button onclick={increment}>Increment</button>
