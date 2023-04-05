<script>
  import { onMount } from "svelte";

  onMount(() => {
    (window.adsbygoogle = window.adsbygoogle || []).push({});
  });
</script>

<svelte:head>
  <title>Startseite - MkaY Development</title>
  <meta
    name="description"
    content="Wir entwickeln und betreiben Webseiten und spezielle Software für ihr Unternehmen. Außerdem helfen wir Ihnen bei der Kommunikation mit ihren Kunden per Email."
  />
  <script
    async
    src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-7626334775469515"
    crossorigin="anonymous"
  ></script>
</svelte:head>

<div class="ads-widget-container">
  <ins class="adsbygoogle"
      style="display:block"
      data-ad-client="ca-pub-7626334775469515"
      data-ad-slot="X0X0X0X0X0X0"
      data-ad-format="auto"
      data-full-width-responsive="true"></ins>
</div>

<div class="grid grid-cols-6 gap-3">
  <div class="col-span-6 md:col-span-3">
    <img
      src="https://avatars.githubusercontent.com/u/20771653?v=4"
      alt=""
      class="w-24 rounded-full mx-auto"
    />
    <h2 class="block text-center mt-3">Jonathan Martz</h2>
    <span class="block text-center">Geschäftsführer & Entwickler</span>
    <p class="text-sm block text-center">
      Herzlich Willkommen bei der MkaY Development UG. Hier findet ihr alle
      Informationen zu meiner Firma. Wir entwickeln kleine Webseite und Services
      für Unternehmen im Oberbergischen Kreis.
    </p>
  </div>
  <div class="col-span-6 md:col-span-3">
    <h2 class="font-bold block text-center text-lg">Verantwortlicher:</h2>
    <p class="block text-center text-sm">
      Jonathan Martz <br />
    </p>
    <h2 class="font-bold block text-center text-lg mt-3">Adresse:</h2>
    <p class="block text-center text-sm">
      Othestrasse 2 <br />
      51702 Bergneustadt <br />
      Germany <br />
    </p>
    <h2 class="font-bold block text-center text-lg mt-3">Kontakt:</h2>
    <p class="block text-center text-sm">
      Tel.: <a href="tel:+49 174 5141698" class="text-blue-600">0174 5141698</a>
      <br />
      Mail:
      <a href="mailto:kontakt@mkay.dev" class="text-blue-600"
        >kontakt@mkay.dev</a
      >
    </p>
  </div>
</div>
