<script>
    import {
        getCategory,
        getCategoryProducts,
    } from "@shopware-pwa/shopware-6-client";
    import { onMount } from "svelte";

    export let identifier;

    let products = [];
    let categorie = {};

    onMount(async () => {
        categorie = await getCategory(identifier);
        let tmp = await getCategoryProducts(identifier);
        products = tmp.elements;
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
            <p class="text-sm">{p.description}</p>
        </div>
        <div class="price">ab {p.calculatedPrice.unitPrice.toFixed(2)} €</div>
    </div>
{/each}
