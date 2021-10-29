<script>
    export let Token;

    let lvlToClass = [
        "text-4xl",
        "text-3xl",
        "text-2xl",
        "text-xl",
        "text-lg",
    ]
</script>

<h1 id="{Token?.text?.toLowerCase()}" class="{lvlToClass[Token?.depth]} text-white font-bold">
    <slot />
</h1>
