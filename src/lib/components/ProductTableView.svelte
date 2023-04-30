<script>
    import { onMount } from "svelte";
    import PocketBase from "pocketbase";
    import { url } from "../../stores/backend";

    export let identifier;

    let products = [];
    let categorie = {};

    onMount(async () => {
        const pb = new PocketBase($url);
        categorie = await pb.collection("categories").getOne(identifier);
        products = (
            await pb
                .collection("products")
                .getList(1, 50, { filter: 'category="' + identifier + '"' })
        ).items;
    });
</script>

{#if categorie.name}
    <h3 class="font-bold mt-6">
        {categorie.name}
    </h3>
{/if}
{#each products as p}
    <div class="flex justify-between mt-3">
        <div class="name">
            {p.name} <br />
            <p class="text-sm">{p.desc}</p>
        </div>
        <div class="price">ab {p.price.toFixed(2)} €</div>
    </div>
{/each}
