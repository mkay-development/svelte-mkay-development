<script>
  import PocketBase from "pocketbase";
  import { onMount } from "svelte";

  let result;
  let projects = [];

  let load = async function () {
    const pb = new PocketBase("https://xano7eir59eemdw.pocketbase.tech");
    result = await pb.collection("projects").getList(1, 9);
    projects = result.items;
  };

  onMount(function () {
    load();
  });
</script>

<h2 class="font-bold text-lg">Projekte</h2>

<div class="grid grid-cols-6">
  {#each projects as project}
    <div class="col-span-6 md:col-span-2">
      <section class="card bg-gray-300 px-2 py-2">
        <img
          src="https://via.placeholder.com/480x320.png?text=MkaY+Development"
          alt=""
        />
        <h2 class="font-bold mt-2">{project.name}</h2>
        <p class="text-sm">{project.desc}</p>
        <div class="actions mt-6 mb-2 text-right">
          <a href={project.url} target="_blank" class="px-2 py-2 bg-red-400 text-sm text-white">Zur Webseite</a>
        </div>
      </section>
    </div>
  {/each}
</div>
<svelte:head>
  <title>Projekte - MkaY Development</title>
  <meta
    name="description"
    content="Hier findest du alle unserere kleinen und großen Projekte."
  />
</svelte:head>
