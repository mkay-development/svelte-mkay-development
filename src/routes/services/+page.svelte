<script>
    import ProductTableView from "$lib/components/ProductTableView.svelte";
    let categories = [
        "aa208bfab4a24771a97fdcb459c4ffb2",
        "1274c1a781934a36a80766b9101055e0",
        "f89966ed05d74d90a8374323ad4171fa",
    ];
</script>

{#each categories as c}
    <ProductTableView identifier={c} />
{/each}
