<script>
  import Logo from "./Logo.svelte";

  const name = "Harun";
  const content = "Hello <strong>Harun</strong>";
</script>

<h1>Hello {name.toUpperCase()}!</h1>
<p>{@html content}</p>
<Logo />

<style>
  h1 {
    color: red;
  }
</style>
