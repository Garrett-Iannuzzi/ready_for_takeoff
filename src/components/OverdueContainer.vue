<template>
  <section class="account-column grid" id="overdue-account-column">
    <div class="account-container-title" id="overdue-account-container-title">
      <h3>Overdue</h3>
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
  name: "OverdueContainer",
}
</script>

<style>
  #overdue-account-container-title > h3{
    color: #B22222;
  }
</style>