
<script>
    export let Articles

    import ListDisplay from "Style/Article/ListDisplay.svelte";
</script>

{#each Articles as Article}
    <ListDisplay Article={Article}/>
{/each}