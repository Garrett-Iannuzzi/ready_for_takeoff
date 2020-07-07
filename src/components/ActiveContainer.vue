<template>
  <section class="account-column grid" id="active-account-column">
    <div class="account-container-title" id="active-account-container-title">
      <h3>Active</h3>
    </div>
    <div class="account-container active-account">
      <ul class="account-data-list">
        <li><label>Name:</label>LastName, FirstName</li>
        <li><label>Email:</label>Email</li>
        <li><label>Phone Number:</label>PhoneNumber</li>
        <li><label>Amount Due:</label>AmountDue</li>
        <li><label>Due Date:</label>DueDate</li>
      </ul>
    </div>     
  </section>
</template>

<script>
export default {
  name: "ActiveContainer"
}
</script>

<style>
  #active-account-container-title > h3 {
    color:#006643;
  }
</style>