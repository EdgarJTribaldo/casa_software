<script>
  import Hero from './components/Hero.svelte';
  import Services from './components/Services.svelte';
</script>

<main>
  <Hero/>
  <Services/>
</main>

<style>
  :global(body) {
    margin: 0;
    padding: 0;
    font-family: 'Inter', sans-serif;
  }

  main {
    width: 100%;
    min-height: 100vh;
  }
</style>
