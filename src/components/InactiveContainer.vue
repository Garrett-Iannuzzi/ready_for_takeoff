<template>
  <section class="account-column grid" id="inactive-account-column">
    <div class="account-container-title" id="inactive-account-container-title">
      <h3>Inactive</h3>
    </div>
      <div class="account-container active-account" v-bind:key="inactiveAcc.id" v-for="inactiveAcc in inactiveAcc">
      <ul class="account-data-list">
        <li><label>Name:</label>{{ inactiveAcc.LastName }}, {{inactiveAcc.FirstName}}</li>
        <li><label>Email:</label>{{inactiveAcc.Email}}</li>
        <li><label>Phone Number:</label>{{ formatPhone(inactiveAcc.PhoneNumber)}}</li>
        <li><label>Amount Due:</label>{{inactiveAcc.AmountDue}}</li>
      </ul>
    </div>    
  </section>
</template>

<script>

export default {
  name: "InactiveContainer",
  props: ["inactiveAcc"],
  methods: {
    formatPhone(num) {
      return `(${num.slice(0, 3)})-${num.slice(3, 6)}-${num.slice(6, 10)}`
    }
  }
}

</script>

<style>
  #inactive-account-container-title > zh3 {
    color:#808080;
  }
</style>