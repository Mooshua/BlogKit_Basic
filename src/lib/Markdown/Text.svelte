<script>
    export let Token
</script>

{#if Token.tokens != undefined}
    <slot />
{:else}
    {@html Token?.text}
{/if}