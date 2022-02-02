<script>
    import {user_store} from "$lib/stores.js";
import PrimaryButton from "./PrimaryButton.svelte";

    let success;

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
<form class="supplier-form rounded border-1 m-auto w-12/12 md:w-120 p-4" on:submit|preventDefault={signUp}>

    <label for="business_type">Business Type</label>
    <select class="w-full" name="business_type">
      <option disabled selected="true">Select</option>
      <option value="Ltd">Ltd</option>
      <option value="Sole trader">Sole trader</option>
      <option value="Partnership">Partnership</option>
      <option value="CIC">CIC</option>
    </select>

    <!-- This data will be more confusing, harder to store and reference and query if with ranges -->
    <label for="staff_number">How many staff?</label>
    <select class="w-full" name="staff_number">
      <option disabled selected="true">Select</option>
      <option value="1">1</option>
      <option value="2 - 5">2 - 5</option>
      <option value="6 - 10">6 - 10</option>
      <option value="11 - 30">11 - 30</option>
      <option value="31 - 50">31 - 50</option>
      <option value="50 or more">50 or more</option>
    </select>

        <!-- This data will be more confusing, harder to store and reference and query if with ranges -->
    <label for="annual turnover">Approxiamate annual turnover</label>
    <select class="w-full" name="annual turnover">
      <option disabled selected="true">Select</option>
      <option value="£5000 - £15000">£5000 - £15000</option>
    </select>

    <label for="company_number">Company Number</label>
    <input class="w-full" name="company_number" placeholder="Companies House check possible">

    <label for="tags">TAGS</label>
    <input class="w-full" name="tags" placeholder="Up to five tags, seperate with commas">


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