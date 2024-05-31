<script>
  import FootLeft from "./FootLeft.vue";
  import FootRight from "./FootRight.vue";
  export default {
    components: {
      FootLeft,
      FootRight,
    },
  };
</script>

<template>
  <footer>
    <div class="container">
      <div class="row">
        <FootLeft />
        <FootRight />
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
  footer {
    background-color: #1a1a1a;
    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding-top: 80px;
      padding-bottom: 80px;
      .row {
        display: flex;
        flex-wrap: wrap;
      }
    }
  }
</style>
