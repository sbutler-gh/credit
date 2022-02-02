<script>
import { page } from "$app/stores";

import { onMount } from "svelte";


    export let clearing_union = "Lancaster's <br> <strong>Trade Credit Mutual</strong>";

    let main_title = "Loading"
    let details_title = "Loading"

    onMount(() => {
        console.log($page);
        if ($page.path == "/onboarding") {
            main_title = "Your Business";
            details_title = "- we only need a little information to get started - first, the basics";
        }
        else if ($page.path == "/onboarding_details") {
            main_title = "The Details";
            details_title = "- this information is optional but can help us build a better network";
        }
        else if ($page.path == "/") {
            // details_title = "This is where you can find out more";
        }
    });
</script>
<div class="header w-12/12 p-2 sm:w-10/12 m-auto">
    <div class="text-center mt-4">
        <!-- <a href="/" class="ml-8 text-lg text-left font-semibold"></a> -->
        <!-- {#if $page.path == "/"}
        <h2 class="text-xl text-center font-semibold mt-4 mb-2">Welcome to</h2>
        <a href="/" class="text-xl mb-4 block m-auto text-orange-700 text-center">{@html clearing_union}</a>
        <h3 class="text-center text mt-4 mb-4 font-semibold">This is where you can find out more</h3>

        {:else}
        <a href="/" class="text-xl mb-4 block m-auto text-orange-700 text-center">{@html clearing_union}</a>
        <hr class="w-10/12 m-auto">
        <h2 class="text-xl text-center font-semibold mt-4">{main_title}</h2>
        <h3 class="text-center text-sm mt-4 mb-4 font-semibold">{details_title}</h3>
        {/if} -->

        {#if $page.path == "/"}
        <h2 class="text-xl text-center font-semibold mt-4 mb-2">Welcome to</h2>
        <a href="/" class="text-xl mb-4 block m-auto text-orange-700 text-center">{@html clearing_union}</a>
        <h3 class="text-center text mt-4 mb-4 font-semibold">This is where you can find out more</h3>

        {:else if $page.path == "/onboarding"}
        <a href="/" class="text-xl mb-4 block m-auto text-orange-700 text-center">{@html clearing_union}</a>
        <hr class="w-10/12 m-auto">
        <h2 class="text-xl text-center font-semibold mt-4">Your Business</h2>
        <h3 class="text-center text-sm mt-4 mb-4 font-semibold">- we only need a little information to get started - first, the basics</h3>

        {:else if $page.path == "/onboarding_details"}
        <a href="/" class="text-xl mb-4 block m-auto text-orange-700 text-center">{@html clearing_union}</a>
        <hr class="w-10/12 m-auto">
        <h2 class="text-xl text-center font-semibold mt-4">The Details</h2>
        <h3 class="text-center text-sm mt-4 mb-4 font-semibold">- this information is optional but can help us build a better network</h3>
        {/if}
  
        <!-- <div class="ml-auto w-8/12 sm:hidden">
          <a href="/suppliers" class="m-auto md:border md:rounded mr-2 md:bg-white text-blue-500 bg-white underline md:no-underline p-0 md:text-black md:px-2 md:py-1 rounded font-semibold md:font-normal">Suppliers</a>
          <a href="/buyers" class="m-auto md:border md:rounded mr-2 md:bg-white text-blue-500 bg-white underline md:no-underline p-0 md:text-black md:px-2 md:py-1  rounded font-semibold md:font-normal">Buyers</a>
          <a href="/manifesto" class="m-auto md:bg-orange-300 text-blue-500 bg-white underline md:no-underline p-0 md:text-black md:px-6 md:py-2  rounded font-semibold md:font-normal">Manifesto</a>
          </div>
        <div class="ml-auto w-max hidden sm:block">
        <a href="/suppliers" class="m-auto md:border md:rounded mr-4 md:bg-white text-blue-500 bg-white underline md:no-underline p-0 md:text-black md:px-2 md:py-2 rounded font-semibold md:font-normal">For Suppliers</a>
        <a href="/buyers" class="m-auto md:border md:rounded mr-4 md:bg-white text-blue-500 bg-white underline md:no-underline p-0 md:text-black md:px-2 md:py-2  rounded font-semibold md:font-normal">For Buyers</a>
        <a href="/manifesto" class="m-auto md:bg-orange-300 text-blue-500 bg-white underline md:no-underline p-0 md:text-black md:px-6 md:py-2  rounded font-semibold md:font-normal">Our Manifesto</a>
        </div> -->
    </div>
    </div>

    <style>
        .header {
            background: #60C2FA
        }
    </style>