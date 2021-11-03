<script>

    import { onMount } from 'svelte';

    onMount(async () => {
		document.body.className += "bg-gray-900"
	});


    import Footer from "./Util/Footer.svelte"

</script>


<!--Primary flexbox-->
<div class="w-screen max-w-full overflow-x-hidden min-h-screen bg-gray-900 flex flex-col md:flex-row md:justify-center">
    <!--Internal width adjustment (center on screen)-->
    <div class="w-full p-4 sm:p-8 md:p-16 lg:w-4/5 xl:w-7/12 2xl:w-5/12">
        <slot />

        <Footer />
    </div>
</div>