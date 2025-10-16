<script>
  const getArticle = async () => {
    let response = await fetch("/article.json");
    return await response.json();
  };
</script>

{#await getArticle()}
  <p>Loading...</p>
{:then article}
  <p>Title: {article.title}</p>
  <p>Content: {article.content}</p>
{:catch err}
  <p>Error: {err.message}</p>
{/await}
