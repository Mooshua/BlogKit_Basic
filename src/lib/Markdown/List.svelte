<script>

    export let value;
    export let meta;
</script>

{#if meta?.ordered }
    <ol class="list-decimal" start="{meta?.ordered || 1}">
        {@html value}
    </ol>
{:else}
    <ul class="list-disc" start="{meta?.ordered || 1}">
        {@html value}
    </ul> 
{/if}

