---
layout: default
title: Refer A Friend
permalink: /refer/
---

<form method="post" class="home-value cta-forms" action="http://formspree.io/Brad@BradCohenHomes.com" onsubmit="return setReturn()">
    <fieldset>
        <p id="thanks"></p>

        <label for="Name">
        Name
        </label>
        <input type="text" name="name" required/>

        <label for="email">
        Email
        </label>
        <input type="text" name="email" required/>

        <label for="phone">
        Phone
        </label>
        <input type="text" name="phone" required/>

        <label for="type">Are they...</label>
        <select name="type" required>
            <option value="Buying" selected="selected">
                Buying
            </option>
            <option value="Selling">
                Selling
            </option>
            <option value="Buying and Selling">
                Buying and Selling
            </option>
        </select>


        <!-- submit! -->
        <input class="submit light-light" type="submit" value="Submit" name="submitSellerForm">
        <span class="asterisk">*</span>required
    </fieldset>
    <!-- Cloud cannon settings field -->
    <div class="hidden">
      <input type="hidden" name="_to" value="{{site.data.settings.client.email}}">
      <input type="hidden" name="_subject" value="Referral form submission from your Vyral Video Blog">
      <input type="text" name="_gotcha">
    </div>
</form>
<script>
function setReturn(){
  localStorage.setItem("thanks", "Your request was sent successfully!");
  document.getElementById("thanks").innerHTML =    localStorage.getItem("thanks");
  localStorage.clear();
}
</script>
