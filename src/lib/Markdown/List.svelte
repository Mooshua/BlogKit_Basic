<script>

    export let Token

</script>

{#if Token?.ordered }
    <ol class="list-decimal" start="{Token?.ordered || 1}">
        <slot />
    </ol>
{:else}
    <ul class="list-disc" start="{Token?.ordered || 1}">
        <slot />
    </ul> 
{/if}

