<script>


    export let Article

    $: Created = (new Date(Article?.article?.createdAt)).toDateString()

</script>

<h1 class="text-5xl font-bold font-mono text-white mt-32">

    {Article?.article?.title}

</h1>

<!--About the author-->
<div class="flex flex-cols space-x-6 text-white my-8">
    <div>
        <img class="w-16 h-16 rounded-full" width="64px" height="64px" src="https://avatars.githubusercontent.com/u/{Article?.author?.id}?v=4" />
    </div>
    <div>
        <p class="text-xl">
            {Article?.author.cached_name || "Mooshua"}
        </p>
        <p>
            {Created}
        </p>
    </div>
</div>

<div class="text-white space-y-4">

    <slot />

</div>

