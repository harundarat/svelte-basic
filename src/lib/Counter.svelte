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

    $inspect(count).with((type, values) => console.info(type, values));
</script>

<h1 class={total % 2 === 0 ? "red" : "blue"}>{count.join(" + ")} = {total}</h1>

<button onclick={increment}>Increment</button>

<style>
    button {
        background-color: forestgreen;
        color: whitesmoke;
    }

    button:hover {
        background-color: green;
    }

    .red {
        background-color: red;
    }

    .blue {
        background-color: blue;
    }
</style>
