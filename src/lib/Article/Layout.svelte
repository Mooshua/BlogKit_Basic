<script>


    export let Article

    import AuthorCard from "Style/User/AuthorCard.svelte"

    $: Created = (new Date(Article?.article?.createdAt)).toDateString()

</script>

<svelte:head>
    <title>
        {Article?.article?.title}
    </title>
    <meta name="description" content={Article?.article?.subtitle} />
</svelte:head>

<div class="px-4 sm:px-8">
    <h1 class="text-5xl font-bold font-mono text-white my-4 mt-32">

        {Article?.article?.title}

    </h1>

    <h3 class="my-4 text-gray-200 font-mono text-xl">
        {Article?.article?.subtitle}
    </h3>

</div>

<AuthorCard User={Article?.author} Subline="On {Created}" />

<div class="text-white space-y-4 px-4 sm:px-8">

    <slot />

</div>

