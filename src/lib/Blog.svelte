<script>
  import Layout from "./Layout.svelte";
</script>

<Layout title="Contoh Blog" footer="2025">
  {#snippet content()}
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Illum numquam ab
      itaque minima nostrum quaerat vero, reiciendis obcaecati ex voluptas dicta
      ratione saepe, in consectetur magnam mollitia sit doloribus inventore!
    </p>
    <p>
      Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ipsum dolorem
      cupiditate molestiae illum possimus corporis. Dolore eius quam corporis
      assumenda ullam accusamus, quasi expedita nostrum. Cupiditate assumenda
      non eius adipisci?
    </p>
  {/snippet}
</Layout>
