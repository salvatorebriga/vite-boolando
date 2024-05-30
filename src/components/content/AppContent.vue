<script>
  import Card from "./Card.vue";
  export default {
    data() {
      return {
        photos: [
          {
            image: "",
            text: "",
          },
          {
            image: "",
            text: "",
          },
          {
            image: "",
            text: "",
          },
          {
            image: "",
            text: "",
          },
        ],
      };
    },
  };
</script>

<template>
  <div class="container">
    <div class="row">
      <div class="col">
        <Card />
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .container {
    max-width: 1200px;
    margin: 0 auto;

    .row {
      display: flex;
      flex-wrap: wrap;
    }
  }
</style>
