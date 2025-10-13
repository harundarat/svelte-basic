<script>
  let count = $state([]);
  // let total = $derived(count.reduce((prev, curr) => prev + curr, 0));

  let total = $derived.by(() => {
    let total = 0;
    for (let i = 0; i < count.length; i++) {
      total += count[i];
    }
    return total;
  });

  const increment = () => count.push(1);
</script>

<h1>{count.join(" + ")} = {total}</h1>

<button onclick={increment}>Increment</button>
