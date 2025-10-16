<script>
  const { id, name, done } = $props();

  const emojis = {
    "1": "💻",
    "2": "🎨",
    "3": "📖",
    "4": "🚀",
  };

  const emoji = emojis[id];
</script>

{emoji}
{#if done}
  <strike>{id} - {name}</strike>
{:else}
  {id} - {name}
{/if}
