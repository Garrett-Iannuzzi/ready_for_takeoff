<template>
  <div id="app">
    <section class="grid grid-sections">
      <Header />
      <main class="content grid" id="home-content">
        <div class="content-title-container">
          <h2>Accounts</h2>
        </div>
        <section class="grid" id="account-grid">
          <ActiveContainer />
          <OverdueContainer />
          <InactiveContainer />
        </section>
      </main>
      <Footer />
    </section>
  </div>
</template>

<script>
import Header from './components/layout/Header'
import Footer from './components/layout/Footer'
import ActiveContainer from './components/ActiveContainer'
import InactiveContainer from './components/InactiveContainer'
import OverdueContainer from './components/OverdueContainer'

export default {
  name: 'App',
  components: {
    Header,
    Footer,
    ActiveContainer,
    InactiveContainer,
    OverdueContainer,
  },
  data() {
    return {
      activeAcc: [],
      overdueAcc: [],
      inactiveAcc: []
    }
  },
  created() {
    return fetch('https://cors-anywhere.herokuapp.com/https://frontiercodingtests.azurewebsites.net/api/accounts/getall')
    .then(data => data.json())
    .then(res => {
      this.activeAcc = res.filter(accInfo => accInfo.AccountStatusId === 0);
      this.overdueAcc = res.filter(accInfo => accInfo.AccountStatusId === 2);
      this.inactiveAcc = res.filter(accInfo => accInfo.AccountStatusId === 1)
    })
    .catch(err => console.log(err))
  }
}
</script>

<style>
      html, body {
        height: 100%;
        width: 100%;
        font-family: Roboto, Helvetica, Arial, sans-serif
      }
      .grid-sections {
        height: 100%;
        grid-template-columns:1fr;
        grid-template-areas:
            "header"
            "main"
            "footer";
        grid-template-rows: 100px 1fr 150px;
      }
      h2 {
        font-size: 2em;
        color:#006643;
      }
      h3 {
        display: block;
        font-size: 1.5em;
      }
      main {
        grid-area: main;
        overflow: scroll;
      }
      .grid {
        display: grid;
      }
      .title-container {
        grid-column-start: 2;
        align-self: center;
      }
      #home-content {
        grid-row-gap: 25px;
        grid-template-rows: 10px 100px auto;
      }
      #account-grid {
        grid-template-columns: 1fr 1fr 1fr;
        grid-row-start: 3;
      }
      .account-column {
        grid-template-rows: 2em repeat(2, 10em);
      }
      .content-title-container {
        justify-self: center;
        height: 1em;
        grid-row-start: 2;
      }
      .account-container {
        justify-self: center;
        height: 5em;
      }
      .account-container-title {
        justify-self: center;
      }
      .account-data-list {
        list-style: none;
      }
      .account-data-list > li {
        margin: 10px 0;
      }
      .account-data-list > li > label {
        font-weight: bold;
        margin: 0 5px 0 0;
      }
</style>
