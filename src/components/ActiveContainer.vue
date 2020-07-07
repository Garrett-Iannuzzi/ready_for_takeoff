<template>
  <section class="account-column grid" id="active-account-column">
    <div class="account-container-title" id="active-account-container-title">
      <h3>Active</h3>
    </div>
    <AccountCard />
  </section>
</template>

<script>
import AccountCard from './AccountCard'

export default {
  name: "ActiveContainer",
  components: {
    AccountCard
  }
}
</script>

<style>
  #active-account-container-title > h3 {
    color:#006643;
  }
</style>