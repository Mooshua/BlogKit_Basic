<script>
import { add_classes } from "svelte/internal"


    export let Article

    $: Created = (new Date(Article?.article?.createdAt)).toDateString()

</script>

<a href="/article/{Article?.article?.id}"class="block text-white">

    <h2 class="text-3xl font-mono font-semibold">
        {Article?.article?.title}
    </h2>
    <h3 class="text-lg font-mono text-gray-300">
        {Article?.article?.subtitle} - <span>{Article?.author?.cached_username}</span>
        <span class="text-gray-300">On</span>
        <span class="text-gray-200">{Created}</span>
    </h3>

</a>