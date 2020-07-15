<template>
  <header class="grid">
    <div class="title-container">
      <h1>Frontier Airlines</h1>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header"
}
</script>

<style>
  header {
    grid-area: header;
    background-color:#006643;
    grid-template-columns: 1% 98% 1%;
  }
  .title-container {
    grid-column-start: 2;
    align-self: center;
  }
  h1 {
    font-size: 3em;
    color: #fff;
    font-weight: bold;
  }
</style>