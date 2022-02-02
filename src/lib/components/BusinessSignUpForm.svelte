<script>
import { goto } from "$app/navigation";

    import {user_store} from "$lib/stores.js";
import PrimaryButton from "./PrimaryButton.svelte";

    let success;

    function dummySignUp(e) {
      var formData = new FormData(e.target);

      goto('/onboarding_details');
    }

    async function signUp(e) {
        var formData = new FormData(e.target);

        let password = Math.random().toString(36).substr(2, 8);

        formData.append('password', password);

        const response = await fetch(`/signup`, {
            method: 'post',
            body: formData
        })

    if (response.ok) {
      let data = await response.json();
      console.log(data);
      // $user_store = data.user;
      // console.log(data.user);
      // localStorage.setItem('user', JSON.stringify(data.user));
    //   return createNewPage(e);
    success = true;
    }

    else {
      console.log(error);
      signup_error = error;
    }
    }
</script>
<form class="supplier-form rounded border-1 m-auto w-12/12 md:w-120 p-4" on:submit|preventDefault={dummySignUp}>
    
  <!-- <h2 class="text-lg font-semibold mt-2 mb-2">Contact Information</h2> -->

  <label for="company_name">Your Name</label>
    <input class="w-full" name="full_name" placeholder="Full name">
    <!-- <div class="flex">
      <div class="mr-1 w-5/12">
    <label for="first_name">First Name*</label>
    <input class="w-11/12" name="first_name" placeholder="First name">
    </div>
    <div class="ml-1 w-5/12">
    <label for="last_name">Last Name*</label>
    <input class="w-11/12" name="last_name" placeholder="Last name">
    </div>
    </div> -->
    <label for="business_name">Business Name</label>
    <input class="w-full" name="business_name" placeholder="Name people know your business by">

    <label for="email">Contact Email Address</label>
    <input class="w-full" type="email" name="email" placeholder="me@company.com">

    <label for="introduction">Who introduced you to Trade Credit Mutual?</label>
    <select class="w-full" name="introduction">
      <option disabled selected="true">Select</option>
      <option value="Michael Hallam">Michael Hallam</option>
      <option value="Peter Walsmely">Peter Walmsley</option>
    </select>

    <!-- <h2 class="text-lg font-semibold mt-8 mb-2">Business Information</h2>

    <label class="mb-2" for="target_industry">Target Industry (check all that apply)*</label>
    <div class="flex"><input name="target_industry" value="Option 1" type="radio" class="mr-2"><label>Option 1</label></div>
    <div class="flex"><input name="target_industry" value="Option 2" type="radio"  class="mr-2"><label>Option 2</label></div>
    <div class="flex"><input name="target_industry" value="Option 3" type="radio"  class="mr-2"><label>Option 3</label></div>
    <label class="mb-2 mt-2"  for="development_stage">Stage of Development*</label>
    <div class="flex"><input name="development_stage" value="Option 1" type="radio" class="mr-2"><label>Option 1</label></div>
    <div class="flex"><input name="development_stage" value="Option 2" type="radio"  class="mr-2"><label>Option 2</label></div>
    <div class="flex"><input name="development_stage" value="Option 3" type="radio"  class="mr-2"><label>Option 3</label></div>
    <label class="mb-2 mt-2"  for="help_request">I need help with the following items (check all that apply)*</label>
    <div class="flex"><input name="help_request" value="Option 1" type="radio" class="mr-2"><label>Option 1</label></div>
    <div class="flex"><input name="help_request" value="Option 2" type="radio"  class="mr-2"><label>Option 2</label></div>
    <div class="flex"><input name="help_request" value="Option 3" type="radio"  class="mr-2"><label>Option 3</label></div>
    <label class="mt-2" for="activities_description">Describe main product/business activities*</label>
    <textarea class="w-10/12" name="activities_description" placeholder="Enter information here***"></textarea> -->
  <PrimaryButton></PrimaryButton>
    {#if success}
    <p class="m-auto text-green-600 text-center mt-2">Success!  We'll be in touch.</p>
    {/if}
</form>

<style>
  label, input, button {
    display: block;
  }

  input, textarea, select {
    margin-bottom: 1.5rem;
    margin-top: 0.25em;
    padding: 5px;
    /* border: solid 0.5px #e2e2e2; */
    /* border-radius: 5px; */
    background: #DCEDF4;
  }

  form {
    /* max-width: 600px; */
  }
</style>