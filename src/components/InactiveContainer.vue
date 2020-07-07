<template>
  <section class="account-column grid" id="inactive-account-column">
    <div class="account-container-title" id="inactive-account-container-title">
      <h3>Inactive</h3>
    </div>
    <AccountCard />
  </section>
</template>

<script>
import AccountCard from './AccountCard'

export default {
  name: "InactiveContainer",
  components: {
    AccountCard
  }
}

</script>

<style>
  #inactive-account-container-title > h3 {
    color:#808080;
  }
</style>