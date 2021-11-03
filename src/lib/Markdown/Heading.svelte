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
<div class="group">
    <h1 id="{snakeCase(Token?.text || "")}" class="{lvlToClass[Token?.depth]} text-white mt-12 font-bold inline-block">
        <!--Add a "link to this header" button-->
        <slot />
    </h1>
    <a href="#{snakeCase(Token?.text || "")}" alt="">
        <svg xmlns="http://www.w3.org/2000/svg" class="inline-block h-4 w-4 bottom-0 text-opacity-0 text-gray-500 group-hover:text-opacity-100" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13.828 10.172a4 4 0 00-5.656 0l-4 4a4 4 0 105.656 5.656l1.102-1.101m-.758-4.899a4 4 0 005.656 0l4-4a4 4 0 00-5.656-5.656l-1.1 1.1" />
        </svg>
    </a>
</div>