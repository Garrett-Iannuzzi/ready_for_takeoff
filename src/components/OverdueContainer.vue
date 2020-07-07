<template>
  <section class="account-column grid" id="overdue-account-column">
    <div class="account-container-title" id="overdue-account-container-title">
      <h3>Overdue</h3>
    </div>
    <AccountCard />
  </section>
</template>

<script>
import AccountCard from './AccountCard';

export default {
  name: "OverdueContainer",
  components: {
    AccountCard
  }
}
</script>

<style>
  #overdue-account-container-title > h3{
    color: #B22222;
  }
</style>