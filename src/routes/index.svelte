<script>
    import BuyingRequestForm from "$lib/components/BuyingRequestForm.svelte";
import InquiriesForm from "$lib/components/InquiriesForm.svelte";
import SignUpForm from "$lib/components/SignUpForm.svelte";
import SupplierSignUpForm from "$lib/components/SupplierSignUpForm.svelte";

let display;
</script>

<div class="text-center">

    <h2 class="mt-4">If you haven’t seen the video yet, we think it gives a good introduction to what we’re about</h2>
    <div class="embed-youtube">
        <iframe width="560" height="315" src="https://www.youtube.com/embed/o9u3q_1MXR8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>
    <h3 class="text my-4 font-semibold">The simple plan</h3>
    <p class="text-left">We’re looking for 100 or more businesses which trade locally, buying and selling, a few times each month.<br><br>
        Simply by listing the invoices they receive from firms in the group (just the amount, and who it’s from), identifying loops allows 10% or more of the debt inside the group to be ‘cleared’ each month - settled without any money changing hands.<br><br>
        If we can do this - improve member business’s cashflow, we’ll have done something.<br>
        </p>

    <h3 class="text-lg my-4">Loops allow clearing</h3>
    <img class="w-full" src="src/lib/3loop-table-after 1.png">
    <p class="text-left">The smallest debt can be cleared around a loop with credit notes. There can be hundreds of loops.</p>


    <h3 class="text-lg my-4">How will it work?</h3>
    <p class="text-left"><strong>Phase 1:</strong> we’ll collect approximate figures from lots of businesses - hopefully yours! We’ll analyse the data and see if there’s a viable group; if there is, we go to ...<br><br>
        <strong>Phase 2:</strong> we’ll invite businesses which the anaylsis suggests will benefit to a pilot, which will last a month or so - at the end of which there will be a clearing event - and we’ll see how much we can really save.<br><br>
        <strong>Phase 3:</strong> we’ll set up a club and invite lots of businesses to become members, clearing every month.</p>

        <h3 class="text-lg my-4">More details, please ...</h3>
        <p class="text-left">Since 30 days to pay is pretty standard, we’ll run a clearing event every month, looking at all the invoices entered since the last event (including any not fully cleared or paid from then) to find the new loops that can be cleared.<br><br>
            Every member will receive a ‘set-off notice’ with full information on the invoices to be affected (consent is checked each time).<br><br>
            Credit notes will be issued for book-keeping.</p>

            <h3 class="text-lg my-4">This is just the start ...</h3>
        <p class="text-left mb-4">Once a club exists, members can choose to do more:</p>
        <ul class="text-left ml-8 list-disc mb-4">
            <li>Bring more trade into the group, by</li>
            <li class="ml-8"> trading preferentially with other members</li>
                <li class="ml-8">inviting new members in</li>
                <li> Clear even more invoices with pooled trade credit</li>
                    <li>Connect with other groups for more and better loops</li>
                        <li> Connect with local shopping vouchers to boost the local economy</li>
        </ul>
        <p class="text-left">All of these can make your pounds go further.</p>
        <br>
        <a href="/onboarding" class="fixed bottom-0 left-0 right-0 mb-2 block m-auto bg-orange-500 text-xl text-black w-8/12 py-2 rounded font-semibold">OK, I’ll give it a go..</a>
</div>
<style>
    .header button  {
        font-size: 16px;
    }
    .main {
        max-width: 800px;
        padding: 1em;
    }
    .embed-youtube {
position: relative;
padding-bottom: 56.25%; /* - 16:9 aspect ratio (most common) */
/* padding-bottom: 62.5%; - 16:10 aspect ratio */
/* padding-bottom: 75%; - 4:3 aspect ratio */
padding-top: 30px;
height: 0;
overflow: hidden;
width: 100%;
}

.embed-youtube iframe,
.embed-youtube object,
.embed-youtube embed {
border: 0;
position: absolute;
top: 0;
left: 0;
width: 100%;
height: 100%;
}
</style>