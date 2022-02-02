<script>
  import "../app.css";
  import Header from "$lib/components/Header.svelte";
</script>
  <Header></Header>
  <div class="main m-auto mb-8">
<slot></slot>
</div>
<style>
      .main {
        max-width: 800px;
        padding: 1em;
    }
</style>