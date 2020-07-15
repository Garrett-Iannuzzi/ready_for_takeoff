<template>
  <footer class="grid">
    <!-- <h6>Footer</h6> -->
    <!-- <p class="copy">&copy;<script>document.write(new Date().getFullYear())</script></p> -->
  </footer>
</template>

<script>
export default {
  name: "Footer"
}
</script>

<style>
  footer {
    grid-area: footer;
    background-color:#006643;
    color: #fff;
    grid-template-columns: 1% 98% 1%;
    grid-template-rows: 5% 90% 5%;
  }
  .copy {
    place-self: end;
    grid-row-start: 2;
    grid-column-start: 2;
  }
</style>