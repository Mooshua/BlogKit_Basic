<script>
    export let Token
</script>

<a class="text-blue-500 visited:text-purple-500" href={Token?.href}>
    <slot />
</a>