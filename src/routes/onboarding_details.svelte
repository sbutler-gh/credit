<script>
    import BusinessDetailsForm from "$lib/components/BusinessDetailsForm.svelte";
import BusinessSignUpForm from "$lib/components/BusinessSignUpForm.svelte";
import BuyingRequestForm from "$lib/components/BuyingRequestForm.svelte";
import InquiriesForm from "$lib/components/InquiriesForm.svelte";
import SignUpForm from "$lib/components/SignUpForm.svelte";
import SupplierSignUpForm from "$lib/components/SupplierSignUpForm.svelte";

let display;
</script>
<!-- <hr>
    <h2 class="text-xl text-center font-semibold mt-4">The Details</h2>
    <h3 class="text-center text-sm mt-4 mb-4 font-semibold">- this information is optional but can help us build a better network</h3> -->

    <BusinessDetailsForm></BusinessDetailsForm>

<style>
    .header button  {
        font-size: 16px;
    }
    .main {
        max-width: 800px;
        /* padding: 0.5em; */
    }
</style>