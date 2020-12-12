<script>
  // export let segment;
  import Header from "./components/Layouts/Header.svelte";
  import Footer from "./components/Layouts/Footer.svelte";

  let year = new Date().getFullYear();
</script>

<div class="wrapper">
  <Header background="#333" />
  <main>
    <slot />
  </main>
  <Footer background="#333" color="#eee">
    ©{year}
    Restore Medical Group is a DBA of Restore Osteo of Colorado, LLC
  </Footer>
</div>

<style>
  .wrapper {
    display: grid;
    grid-template-rows: auto 1fr auto;
    min-height: 100vh;
  }
  main {
    background: linear-gradient(
      to bottom right,
      transparent,
      rgba(0, 0, 0, 0.24)
    );
  }
</style>
