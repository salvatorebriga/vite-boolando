<script>
  export default {
    name: "Logo",
  };
</script>
<template>
  <div class="col">
    <img src="/img/boolean-logo.png" alt="logo" />
  </div>
</template>

<style lang="scss" scoped>
  .col {
    width: 40%;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 20px;

    img {
      width: 175px;
    }
  }
</style>
