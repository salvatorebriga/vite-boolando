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
  <div class="col">
    <div class="card">
      <img :src="photo.frontImage" alt="product" />
      <p>{{ photo.brand }}</p>
      <h3>{{ photo.name }}</h3>
      <span class="orange">{{ photo.price }}$ </span>
      <span class="line-throught">{{ photo.price }}$ </span>
      <div class="labels">
        <div v-for="badge in photo.badges" :class="badge.type">
          <p>{{ badge.value }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .col {
    margin: 20px;
    width: calc(100% / 3 - 40px);

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

      .orange {
        color: red;
        font-weight: 600;
      }

      .line-throught {
        text-decoration: line-through;
        color: black;
        font-weight: 600;
      }

      .labels {
        position: relative;
        bottom: 150px;
        display: flex;
        color: white;
        font-size: 15px;
        font-weight: 800;

        .discount {
          width: 50px;
          background-color: red;
          display: grid;
          place-items: center;
        }
        .tag {
          width: 150px;
          background-color: green;
          display: grid;
          place-items: center;
        }
      }
    }
  }
</style>
