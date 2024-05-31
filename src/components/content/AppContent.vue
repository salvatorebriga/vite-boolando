<script>
  import products from "/src/data/db.json";
  import Card from "./Card.vue";
  export default {
    data() {
      return {
        products,
      };
    },

    components: {
      Card,
    },
  };
</script>

<template>
  <div class="container">
    <div class="row">
      <Card
        v-for="(photo, index) in products.products"
        :key="index"
        :photo="photo"
      />
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .container {
    max-width: 1200px;
    margin: 0 auto;
    padding-top: 80px;

    .row {
      display: flex;
      flex-wrap: wrap;
    }
  }
</style>
