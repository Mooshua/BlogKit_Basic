<script>

    export let Token

</script>

{#if Token?.ordered }
    <ol class="list-decimal space-y-4" start="{Token?.ordered || 1}">
        <slot />
    </ol>
{:else}
    <ul class="list-disc space-y-4" start="{Token?.ordered || 1}">
        <slot />
    </ul> 
{/if}

