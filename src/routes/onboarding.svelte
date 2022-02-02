<script>
    import BusinessSignUpForm from "$lib/components/BusinessSignUpForm.svelte";
import BuyingRequestForm from "$lib/components/BuyingRequestForm.svelte";
import InquiriesForm from "$lib/components/InquiriesForm.svelte";
import SignUpForm from "$lib/components/SignUpForm.svelte";
import SupplierSignUpForm from "$lib/components/SupplierSignUpForm.svelte";

let display;
</script>
<!-- <hr>
    <h2 class="text-xl text-center font-semibold mt-4">Your Business</h2>
    <h3 class="text-center text-sm mt-4 mb-4 font-semibold">- we only need a little information to get started - first, the basics</h3> -->

    <BusinessSignUpForm></BusinessSignUpForm>

<style>
        
    .main {
        max-width: 800px;
        /* padding: 0.5em; */
    }
</style>