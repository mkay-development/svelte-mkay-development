<script>
  import "../tailwind.css";
  import Header from "$lib/components/Header.svelte";
  import Footer from "$lib/components/Footer.svelte";

  import { setup } from "@shopware-pwa/shopware-6-client";
  setup({
    endpoint: "https://shopware.mkay.dev",
    accessToken: "SWSCCELNZGZUBXPVT2O0OVFMYG",
  });
</script>

<svelte:head
  ><script
    defer
    data-domain="mkay-development.de"
    src="https://bhkenqpeta4iu6t.plausible.dev/js/script.js"
  ></script>
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
