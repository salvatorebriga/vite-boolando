<script>
  export default {
    name: "Card",
    props: {
      photo: {
        type: Object,
        required: true,
      },
    },
  };
</script>
<template>
  <div class="card">
    <img :src="photo.src" alt="product" />
    <p>{{ photo.brand }}</p>
    <h3>{{ photo.text }}</h3>
    <span>{{ photo.price }}$ </span>
    <span>{{ photo.price }}$ </span>
    <div class="labels">
      <div class="red">
        <p>-{{ photo.discount }}%</p>
      </div>
      <div class="green" v-show="photo.sustein === true">
        <p>Susteinability</p>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .card {
    img {
      width: 100%;
      margin-bottom: 2px;
    }

    h3 {
      margin-bottom: 2px;
    }

    p {
      margin-bottom: 2px;
    }

    .labels {
      position: relative;
      bottom: 150px;
      display: flex;
      color: white;
      font-size: 15px;
      font-weight: 800;

      .red {
        width: 50px;
        background-color: red;
        display: grid;
        place-items: center;
      }
      .green {
        width: 150px;
        background-color: green;
        display: grid;
        place-items: center;
      }
    }
  }
</style>
