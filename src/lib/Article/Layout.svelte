<script>


    export let Article

</script>

<h1 class="text-7xl font-bold text-white">

    {Article?.article?.title}

</h1>

<div class="text-white space-y-4">

    <slot />

</div>

