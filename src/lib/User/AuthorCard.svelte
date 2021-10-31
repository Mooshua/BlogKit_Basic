<script>

    export let User
    export let Subline

</script>

<!--About the author-->
<a href="/user/{User?.id}" class="block p-4 sm:p-8 flex border-16 border-gray-700 border-opacity-0 flex-cols space-x-6 text-white my-12 transition rounded-lg hover:border-opacity-100 hover:bg-gray-700">
    <div>
        <img class="w-16 h-16 rounded-full" width="64px" height="64px" src="https://avatars.githubusercontent.com/u/{User?.id}?v=4" />
    </div>
    <div>
        <p class="text-xl">
            {User?.cached_username}
        </p>
        <p class="font-mono text-gray-300">
            {Subline}
        </p>
    </div>
</a>