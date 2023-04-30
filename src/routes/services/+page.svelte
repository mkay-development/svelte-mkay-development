<script>
    import ProductTableView from "$lib/components/ProductTableView.svelte";
    import { onMount } from "svelte";
    import { url } from "../../stores/backend";
    import PocketBase from "pocketbase";

    let categories = [];

    onMount(async function () {
        const pb = new PocketBase($url);
        const result = await pb.collection("categories").getList(1, 50);
        categories = result.items;
    });
</script>

<div class="grid grid-cols-6 gap-3">
    {#each categories as c}
        <div class="col-span-6 md:col-span-3">
            <ProductTableView identifier={c.id} />
        </div>
    {/each}
</div>
