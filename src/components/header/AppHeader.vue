<script>
  import ColLeft from "./ColLeft.vue";
  import Logo from "./Logo.vue";
  import ColRight from "./ColRight.vue";
  export default {
    name: "AppHeader",
    components: {
      ColLeft,
      ColRight,
      Logo,
    },
  };
</script>

<template>
  <header>
    <div class="container">
      <div class="row">
        <ColLeft />
        <Logo />
        <ColRight />
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
  header {
    background-color: orange;
    position: fixed;
    z-index: 2;
    box-shadow: 0px 0.2px 0.2px #ff6900;
    border: 0.1px solid rgb(0, 0, 0);
    width: 100%;

    .container {
      max-width: 1200px;
      margin: 0 auto;

      .row {
        display: flex;
        flex-wrap: wrap;
      }
    }
  }
</style>
