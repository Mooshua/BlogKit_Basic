
<!--Primary flexbox-->
<div class="w-screen min-h-screen bg-gray-900 flex flex-col md:flex-row md:justify-center">
    <!--Internal width adjustment (center on screen)-->
    <div class="w-full p-4 sm:p-8 md:p-16 lg:w-4/5 xl:w-2/3">
        <slot />
    </div>
</div>