<script>
  import { toDisplayString } from "vue";

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
      <img
        class="front"
        :src="`/public/img/${photo.frontImage}`"
        alt="product front"
      />
      <img
        class="back"
        :src="`/public/img/${photo.backImage}`"
        alt="product back"
      />
      <p>{{ photo.brand }}</p>
      <h3>{{ photo.name }}</h3>
      <span class="orange">{{ photo.price }}$ </span>
      <span class="line-throught">{{ photo.price }}$ </span>
      <div class="labels">
        <div v-for="badge in photo.badges" :class="badge.type">
          <p>{{ badge.value }}</p>
        </div>
      </div>
      <div class="hearth">
        <span
          :class="{ red: photo.isInFavorites }"
          @click="photo.isInFavorites = !photo.isInFavorites"
          >&#10084;
        </span>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .col {
    margin: 20px;
    width: calc(100% / 3 - 40px);

    .card {
      position: relative;
      img {
        width: 100%;
        margin-bottom: 2px;
      }

      .front {
        display: block;
      }

      .back {
        display: none;
      }

      &:hover {
        .front {
          display: none;
        }

        .back {
          display: block;
        }
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
        position: absolute;
        bottom: 120px;
        display: flex;
        gap: 5px;
        color: white;
        font-size: 15px;
        font-weight: 600;

        .discount {
          width: auto;
          padding: 5px;
          background-color: red;
          display: grid;
          place-items: center;
        }
        .tag {
          width: auto;
          padding: 5px;
          background-color: green;
          display: grid;
          place-items: center;
        }
      }

      .hearth {
        position: absolute;
        right: 0px;
        top: 25px;
        padding: 10px;
        padding-left: 20px;
        padding-right: 20px;
        background-color: white;

        span {
          font-size: 25px;

          &:hover {
            color: red;
            cursor: pointer;
          }
        }

        .red {
          color: red;
        }
      }
    }
  }

  @media screen and (max-width: 1000px) {
    .col {
      margin: 20px;
      width: calc(100% / 2 - 40px);
      .card {
        .labels {
          font-size: 12px;
        }
      }
    }
  }
  @media screen and (max-width: 620px) {
    .col {
      margin: 20px;
      width: 100%;
      .card {
        .labels {
          font-size: 20px;
        }
      }
    }
  }
</style>
