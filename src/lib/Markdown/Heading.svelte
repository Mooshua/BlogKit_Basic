<script>
    import { snakeCase } from "snake-case";
    export let Token;

    let lvlToClass = [
        "text-4xl",
        "text-3xl",
        "text-2xl",
        "text-2xl",
        "text-xl",
        "text-lg",
    ]
</script>
<a href="#{snakeCase(Token?.text || "")}" alt="">
    <h1 id="{snakeCase(Token?.text || "")}" class="{lvlToClass[Token?.depth]} text-white mt-12 font-bold">
        <!--Add a "link to this header" button-->
        <slot />
    </h1>
</a>