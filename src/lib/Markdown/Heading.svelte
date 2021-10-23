<script>
    export let value = ""
    export let meta = ""

    let lvlToClass = [
        "text-4xl",
        "text-3xl",
        "text-2xl",
        "text-xl",
        "text-lg",
    ]
</script>

<h1 class="{lvlToClass[meta]} text-white font-bold">
    {value}
</h1>

<slot />