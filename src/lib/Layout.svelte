<script>

    import { onMount } from 'svelte';

    onMount(async () => {
		document.body.className += "bg-gray-900"
	});


    import Footer from "./Util/Footer.svelte"

</script>


<!--Primary flexbox-->
<div class="w-screen min-h-screen bg-gray-900 flex flex-col md:flex-row md:justify-center">
    <!--Internal width adjustment (center on screen)-->
    <div class="w-full p-4 sm:p-8 md:p-16 lg:w-1/2 xl:w-1/3">
        <slot />

        <Footer />
    </div>
</div>