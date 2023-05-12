<script>
  import Fa from "svelte-fa";
  import {
    faCode,
    faServer,
    faEnvelope,
  } from "@fortawesome/free-solid-svg-icons";
  import { onMount } from "svelte";
  import { page } from "$app/stores";
  let info = false;

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
        <img src="/images/logo.png" class="h-20 bg-white rounded-lg" alt=""/>
      </a>
    </h1>
    <nav class="hidden md:block">
      <ul class="flex space-x-5 mb-2 mt-1">
        <li><a href="/projects/" class="hover:font-bold">Projekte</a></li>
        <li><a href="/services/" class="hover:font-bold">Services</a></li>
        <li><a href="/customers/" class="hover:font-bold">Kunden</a></li>
        <li><a href="/impressum/" class="hover:font-bold">Impressum</a></li>
      </ul>
      <section class="actions grid grid-cols-6">
        <a href="mailto:anfrage@jonathan-martz.de" class="block text-center text-white bg-green-700 px-2 py-2 col-span-">Anfrage schicken</a>
      </section>
    </nav>
  </div>
  <section class="note text-red-600 bg-white my-5 text-center py-2 px-2">
    Diese Firma exestiert noch nicht, befindet sich aber in der Gründung. <br />
    Startdatum ist der 01.07.2023 als Jonathan Martz Softwareentwicklung.
  </section>
  {#if info}
    <div class="div info-graphic">
      <div class="grid grid-cols-6 gap-3">
        <div class="col-span-6 md:col-span-3 mt-12 md:mt-16 text-white">
          <h2 class="font-bold text-2xl mb-6">Web Development & Web Hosting</h2>
          <p>


            Willkommen bei der Jonathan Martz Softwareentwicklung - Ihrem Partner für Webhosting und Webdevelopment!
            
            Wir bieten zuverlässiges und schnelles Webhosting für Websites jeder Größe und Komplexität. Egal, ob Sie eine kleine Unternehmenswebsite oder eine große E-Commerce-Plattform betreiben möchten, wir haben die perfekte Hosting-Lösung für Sie. Unsere Server sind hochperformant und werden rund um die Uhr überwacht, um eine maximale Verfügbarkeit Ihrer Website zu gewährleisten.
            <br><br>

            Unsere Leidenschaft für Qualität und Kundenzufriedenheit treibt uns an, Ihnen die besten Lösungen für Ihre Webhosting- und Webdevelopment-Bedürfnisse anzubieten. Kontaktieren Sie uns noch heute und lassen Sie uns gemeinsam an Ihrem Erfolg arbeiten!
          </p>
        </div>
        <div class="col-span-6 md:col-span-3">
          <img src="assets/home-font.png" class="z-10" alt="" />
        </div>
        <div class="col-span-6 mt-12 mb-6">
          <section class="actions text-center text-white">
            <span class="leading-10"
              >Schick uns ne Mail an <a
                href="mailto:hallo@jonathan-martz.de"
                class="text-emerald-400 bg-black rounded-lg px-2 py-2"
                >hello@jonathan-martz.de</a
              >
              oder rufe uns an unter
              <a
                href="tel:+49 174 51 41 698"
                class="text-emerald-400 bg-black px-2 py-2 rounded-lg mx-2"
                >0174 51 41 698</a
              >.</span
            >
          </section>
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
