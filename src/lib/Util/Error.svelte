<script>

    export let Code = 1

    export let Reason = ""



</script>

<div>

    <h1 class="text-white text-7xl font-black my-4">{Code}</h1>
    <div class="bg-gray-800 p-4 px-6 rounded-lg max-w-max my-8 text-yellow-500">
        {Reason}
    </div>
    <p class="text-gray-300 text-xl">That's an Error!</p>

    {#if Code == 404}

        <p class="text-gray-300">The content that you are looking for was likely deleted or moved elsewhere.</p>

    {/if}

</div>