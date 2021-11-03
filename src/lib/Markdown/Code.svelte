<script>

    

    export let Token

    let ShowHintDebounce = false
    let ShowHint = false

    function ButtonClick(ev) {
        navigator.clipboard.writeText(Token?.text)

        if (!ShowHintDebounce) {
            ShowHintDebounce = true
            ShowHint = true
            setTimeout(() => {
                ShowHint = false
                ShowHintDebounce = false
            }, 3000)
        }
    }


    $: Highlighted = Token.text
</script>
<div class="bg-gray-800 rounded-lg p-6 relative font-mono whitespace-pre-line">
    {@html Highlighted}
    <button on:click={ButtonClick} class="absolute top-2 right-2 p-2 bg-gray-700 rounded">

        {#if ShowHint}
            <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 text-green-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
            </svg>
            
        {:else}
            <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 5H6a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2v-1M8 5a2 2 0 002 2h2a2 2 0 002-2M8 5a2 2 0 012-2h2a2 2 0 012 2m0 0h2a2 2 0 012 2v3m2 4H10m0 0l3-3m-3 3l3 3" />
            </svg>
        {/if}
        
        
        
        
    </button>
</div> 

