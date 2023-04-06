<script>
  import "../tailwind.css";
  import Header from "$lib/components/Header.svelte";
  import Footer from "$lib/components/Footer.svelte";
</script>

<svelte:head>
  <script defer data-domain="mkay-development.de" src="https://tracking.mkay.dev/js/script.js"></script>
</svelte:head>

<div class="header-background">
  <Header />
  <img src="assets/home-bottom-shape.png" class="" alt="" />
</div>

<main class="mx-auto max-w-5xl my-2 px-2 py-2"><slot /></main>
<Footer />

<style>
  .header-background {
    background: linear-gradient(
      to bottom,
      #370b6f,
      #00429b,
      #006dba,
      #0095ce,
      #2dbcdc
    );
  }
</style>