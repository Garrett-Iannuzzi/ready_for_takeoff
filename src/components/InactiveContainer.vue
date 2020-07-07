<template>
  <section class="account-column grid" id="inactive-account-column">
    <div class="account-container-title" id="inactive-account-container-title">
      <h3>Inactive</h3>
    </div>
    <div class="account-container inactive-account">
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
  name: "InactiveContainer"
}
</script>
<style>
  #inactive-account-container-title > h3 {
    color:#808080;
  }
</style>