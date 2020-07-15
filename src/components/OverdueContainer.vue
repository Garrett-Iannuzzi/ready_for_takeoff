<template>
  <section class="account-column grid" id="overdue-account-column">
    <div class="account-container-title" id="overdue-account-container-title">
      <h3>Overdue</h3>
    </div>
    <div class="account-container active-account" v-bind:key="overdueAcc.id" v-for="overdueAcc in overdueAcc">
      <ul class="account-data-list">
        <li><label>Name:</label>{{ overdueAcc.LastName }}, {{overdueAcc.FirstName}}</li>
        <li><label>Email:</label>{{overdueAcc.Email}}</li>
        <li><label>Phone Number:</label>{{formatPhone(overdueAcc.PhoneNumber)}}</li>
        <li><label>Amount Due:</label>${{overdueAcc.AmountDue}}</li>
        <li><label>Due Date:</label>{{formatDate(overdueAcc.PaymentDueDate)}}</li>
      </ul>
    </div>    
  </section>
</template>

<script>

export default {
  name: "OverdueContainer",
  props: ["overdueAcc"],
  methods: {
    formatDate(str) {
      const date = str.slice(0, 10).split('-').reverse()
      return `${date[0]}/${date[1]}/${date[2]}`
    },
    formatPhone(num) {
      return `(${num.slice(0, 3)})-${num.slice(3, 6)}-${num.slice(6, 10)}`
  }
  }
}
</script>

<style>
  #overdue-account-container-title > h3{
    color: #B22222;
  }
</style>