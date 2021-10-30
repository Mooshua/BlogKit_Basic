<script>

    export let Token;
</script>

<div class="my-4 space-y-4">
    <div class="w-full overflow-hidden flex justify-center sm:transform-gpu sm:scale-x-110 rounded-2xl transition-shadow hover:shadow-lg">
        <img src={Token?.href} alt={Token?.text} class="min-w-full h-auto rounded-lg">
    </div>
    <div>
        <p class="text-center text-gray-300 mb-8">
            {@html Token?.text}
        </p>
    </div>
</div>
