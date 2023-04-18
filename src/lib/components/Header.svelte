<script>
  import Fa from "svelte-fa";
  import {
    faCode,
    faServer,
    faEnvelope,
  } from "@fortawesome/free-solid-svg-icons";
  import { onMount } from "svelte";
  import { page } from "$app/stores";
  import {
    addProductToCart,
    getCart,
    getProduct,
  } from "@shopware-pwa/shopware-6-client";
  let info = false;
  let total = 0;
  let items = [];

  $: $page,
    (function () {
      if ($page.route.id == "/") {
        info = true;
      } else {
        info = false;
      }
    })();

  onMount(async function () {
    if ($page.route.id == "/") {
      info = true;
    }

  });
</script>

<header class="mx-auto max-w-5xl mb-2 px-2 py-2">
  <div class="content flex justify-between text-white">
    <h1 class="text-xl font-bold">
      <a href="/" class="flex">
        <span class="text-4xl font-bold">&#123;</span>
        <div class="logo flex flex-col mt-1.5 mx-2">
          <span class="name text-xs text-center">MkaY Development</span>
          <span class="legal-form text-xs text-center font-normal"
            >UG haftungsbeschränkt</span
          >
        </div>
        <span class="text-4xl font-bold">&#125;</span>
      </a>
    </h1>
    <nav class="hidden md:block">
      <ul class="flex space-x-5 mt-2">
        <li><a href="/projects/" class="hover:font-bold">Projekte</a></li>
        <li><a href="/customers/" class="hover:font-bold">Kunden</a></li>
        <li><a href="/kontakt/" class="hover:font-bold">Kontakt</a></li>
        <li><a href="/impressum/" class="hover:font-bold">Impressum</a></li>
      </ul>
    </nav>
  </div>
  <section class="note text-red-600 bg-white my-5 text-center py-2 px-2">
    Diese Firma exestiert noch nicht, diese Webseite ist nur eine Vorbereitung
    auf zukünftige Projekte. <br />
    Es gibt noch keine aktuellen Projekt die offiziell umgesetzt sind , nur Test
    Projekte.
  </section>
  {#if info}
    <div class="div info-graphic">
      <div class="grid grid-cols-6 gap-3">
        <div class="col-span-6 md:col-span-3 mt-12 md:mt-24 text-white">
          <h2 class="font-bold text-2xl mb-6">Web Development & Web Hosting</h2>
          <p>
            Wir entwickeln und betreiben Webseiten und spezielle Software für
            ihr Unternehmen. Außerdem helfen wir ihnen bei der Kommunikation mit
            ihren Kunden per Email. Dazu setzen wir auf moderne Technologien wie
            Laravel, VueJs und Svelte. <br /> Melde dich jetzt für ein unverbindliches
            Angebot.
          </p>
          <br />
          <p>
            Wir entwickeln und betreiben Webseiten und spezielle Software für
            ihr Unternehmen. Außerdem helfen wir ihnen bei der Kommunikation mit
            ihren Kunden per Email. Dazu setzen wir auf moderne Technologien wie
            Laravel, VueJs und Svelte. <br /> Melde dich jetzt für ein unverbindliches
            Angebot.
          </p>
        </div>
        <div class="col-span-6 md:col-span-3">
          <img src="assets/home-font.png" class="z-10" alt="" />
        </div>
        <div class="col-span-6">
          <hr class="border-2 mt-12 mb-12" />
          <h2 class="font-bold text-white text-lg mb-6">Was tun wir ?</h2>
        </div>

        <div class="col-span-6 md:col-span-2 text-white">
          <Fa icon={faCode} size="4x" class="mx-auto mb-5" />
          <h2 class="block text-center font-bold">Webdevelopment</h2>
          <p class="text-sm block text-center mt-3">
            Lorem ipsum dolor, sit amet consectetur adipisicing elit. Possimus
            exercitationem cupiditate sequi consectetur fuga, repellat, tempora
            doloremque quam, dicta quibusdam debitis sunt quas qui accusantium
            beatae facere minima odio odit.
          </p>
        </div>
        <div class="col-span-6 md:col-span-2 text-white">
          <Fa icon={faServer} size="4x" class="mx-auto mb-5" />
          <h2 class="block text-center font-bold">Webhosting</h2>
          <p class="text-sm block text-center mt-3">
            Lorem ipsum dolor, sit amet consectetur adipisicing elit. Possimus
            exercitationem cupiditate sequi consectetur fuga, repellat, tempora
            doloremque quam, dicta quibusdam debitis sunt quas qui accusantium
            beatae facere minima odio odit.
          </p>
        </div>
        <div class="col-span-6 md:col-span-2 text-white">
          <Fa icon={faEnvelope} size="4x" class="mx-auto mb-5" />
          <h2 class="block text-center font-bold">Mail Verwaltung</h2>
          <p class="text-sm block text-center mt-3">
            Lorem ipsum dolor, sit amet consectetur adipisicing elit. Possimus
            exercitationem cupiditate sequi consectetur fuga, repellat, tempora
            doloremque quam, dicta quibusdam debitis sunt quas qui accusantium
            beatae facere minima odio odit.
          </p>
        </div>
      </div>
    </div>
  {/if}
</header>
