<script>
  import "../app.css";
  import Header from "$lib/components/Header.svelte";
</script>
<svelte:head>
  <title>Lancaster's Trade Credit Mutual</title>
</svelte:head>
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