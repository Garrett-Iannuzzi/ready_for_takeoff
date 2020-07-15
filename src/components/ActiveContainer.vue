<template>
  <section class="account-column grid" id="active-account-column">
    <div class="account-container-title" id="active-account-container-title">
      <h3>Active</h3>
    </div>
    <div class="account-container active-account" v-bind:key="activeAcc.id" v-for="activeAcc in activeAcc">
      <ul class="account-data-list">
        <li><label>Name:</label>{{ activeAcc.LastName }}, {{activeAcc.FirstName}}</li>
        <li><label>Email:</label>{{activeAcc.Email}}</li>
        <li><label>Phone Number:</label>{{ formatPhone(activeAcc.PhoneNumber)}}</li>
        <li><label>Amount Due:</label>${{activeAcc.AmountDue}}</li>
        <li><label>Due Date:</label>{{ formatDate(activeAcc.PaymentDueDate)}}</li>
      </ul>
    </div>     
  </section>
</template>

<script>
export default {
    name: "ActiveContainer",
    props: ["activeAcc"],
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
  #active-account-container-title > h3 {
    color:#006643;
  }
</style>