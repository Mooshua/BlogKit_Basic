<script>

    export let Token
</script>

<div class="overflow-x-auto w-full pb-2">
    <div class="table border-collapse w-max border-1 border-gray-700">
    <div class="table-header-group">
        {#each Token?.header as Header}

            <div class="table-cell p-2 border border-gray-700 text-center text-sm text-gray-300 uppercase font-semibold">
            
                <!--Manually return to dive-->
                <!--Since the markdown diver does not handle tables-->
                <slot Custom={Header?.tokens} />
                
            </div>

        {/each}
    </div>

    {#each Token?.rows as Row}

        <div class="table-row">
            
            {#each Row as Col}

                <div class="table-cell p-2 border border-gray-700">

                    <slot Custom={Col?.tokens} />

                </div>

            {/each}

        </div> 

    {/each}
</div>
</div> 
